Aby na bieżąco dołączać zmiany do ostatniego wykonanego commita, należy do polecenia `git commit` dodać przełącznik `--amend`, np:
`git commit -a --amend`.

Aby połączyć kilka commitów w jeden, trzeba wykonać rebase i squash
`git rebase -i HEAD~2`
gdzie "2" to ilość commitów wstecz, które chcemy połączyć. Spowoduje to otwarcie pliku tekstowego, w którym należy oznaczyć, które commity chcemy połączyć (zmienić `pick` na `s`). Przykładowo jeśli chcemy połączyć 3 ostatnie commity to po kolei:

* `git rebase -i HEAD~3`

Otwiera się plik tekstowy:

```
pick aaa3e33 Dodano wiecej czegos tam
pick 27f2361 Dodano cos tam
pick 2273a6f Dodano infrastrukture projektu
```
i zmieniamy to na (pierwszy `pick` zostaje, `s` to skrót od słowa *squash*):

```
pick aaa3e33 Dodano wiecej czegos tam
s 27f2361 Dodano cos tam
s 2273a6f Dodano infrastrukture projektu
```
Zapisujemy i zamykamy edytor, git spróbuje teraz połączyć commity. Jeśli wszystko przebiegnie pomyślnie, zostaniemy poproszeni jeszcze o podanie treści wiadomości nowego commita: znowu otworzy się edytor tekstowy, w którym będą wszystkie wiadomości z łączonych commitów, należy je usunąć i wpisać tam krótki opis zmian.

Zakończenie procesu zostanie potwierdzone komunikatem `Successfully rebased and updated refs/heads/XXX` lub podobnym.

Wykonanie `git push` w tym momencie najprawdopodobniej zakończy się niepowodzeniem. Aby zaktualizować repozytorium zdalne (na GitHubie) należy zmusić gita do nadpisania commitów używając przełącznika `-f` (*force*):

`git push -f`