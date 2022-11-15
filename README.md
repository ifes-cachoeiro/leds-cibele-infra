# Leds | Cibele Infra
## Infrastructure of Cibele project 
## Orchestrated with Lightweight Kubernetes - K3s

[![love](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com) [![open](https://forthebadge.com/images/badges/open-source.svg)](https://forthebadge.com)  [![forthebadge](data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMTguNzkiIGhlaWdodD0iMzUiIHZpZXdCb3g9IjAgMCAxMTguNzkgMzUiPjxyZWN0IGNsYXNzPSJzdmdfX3JlY3QiIHg9IjAiIHk9IjAiIHdpZHRoPSI2NC44OSIgaGVpZ2h0PSIzNSIgZmlsbD0iI0QzNUIwOSIvPjxyZWN0IGNsYXNzPSJzdmdfX3JlY3QiIHg9IjYyLjg5IiB5PSIwIiB3aWR0aD0iNTUuOTAwMDAwMDAwMDAwMDA2IiBoZWlnaHQ9IjM1IiBmaWxsPSIjRTY4MDM5Ii8+PHBhdGggY2xhc3M9InN2Z19fdGV4dCIgZD0iTTE0LjA4IDE5LjE2TDE0LjA4IDE5LjE2TDE0LjA4IDEzLjQ3TDE1LjU2IDEzLjQ3TDE1LjU2IDE5LjE4UTE1LjU2IDIwLjAzIDE1Ljk5IDIwLjQ4UTE2LjQzIDIwLjkzIDE3LjI3IDIwLjkzTDE3LjI3IDIwLjkzUTE4Ljk4IDIwLjkzIDE4Ljk4IDE5LjEzTDE4Ljk4IDE5LjEzTDE4Ljk4IDEzLjQ3TDIwLjQ2IDEzLjQ3TDIwLjQ2IDE5LjE3UTIwLjQ2IDIwLjUzIDE5LjU5IDIxLjMyUTE4LjcyIDIyLjEyIDE3LjI3IDIyLjEyTDE3LjI3IDIyLjEyUTE1LjgxIDIyLjEyIDE0Ljk0IDIxLjMzUTE0LjA4IDIwLjU1IDE0LjA4IDE5LjE2Wk0yNC41OSAxOS40MkwyNC41OSAxOS40MkwyNi4wOCAxOS40MlEyNi4wOCAyMC4xNSAyNi41NiAyMC41NVEyNy4wNCAyMC45NSAyNy45MyAyMC45NUwyNy45MyAyMC45NVEyOC43MSAyMC45NSAyOS4xMCAyMC42M1EyOS40OSAyMC4zMiAyOS40OSAxOS44MEwyOS40OSAxOS44MFEyOS40OSAxOS4yNCAyOS4wOSAxOC45NFEyOC43MCAxOC42MyAyNy42NiAxOC4zMlEyNi42MyAxOC4wMSAyNi4wMiAxNy42M0wyNi4wMiAxNy42M1EyNC44NiAxNi45MCAyNC44NiAxNS43MkwyNC44NiAxNS43MlEyNC44NiAxNC42OSAyNS43MCAxNC4wMlEyNi41NCAxMy4zNSAyNy44OCAxMy4zNUwyNy44OCAxMy4zNVEyOC43NyAxMy4zNSAyOS40NyAxMy42OFEzMC4xNyAxNC4wMSAzMC41NiAxNC42MVEzMC45NiAxNS4yMiAzMC45NiAxNS45NkwzMC45NiAxNS45NkwyOS40OSAxNS45NlEyOS40OSAxNS4yOSAyOS4wNyAxNC45MVEyOC42NSAxNC41NCAyNy44NyAxNC41NEwyNy44NyAxNC41NFEyNy4xNCAxNC41NCAyNi43NCAxNC44NVEyNi4zNCAxNS4xNiAyNi4zNCAxNS43MUwyNi4zNCAxNS43MVEyNi4zNCAxNi4xOCAyNi43NyAxNi41MFEyNy4yMSAxNi44MSAyOC4yMCAxNy4xMFEyOS4yMCAxNy40MCAyOS44MCAxNy43OFEzMC40MSAxOC4xNiAzMC42OSAxOC42NVEzMC45NyAxOS4xMyAzMC45NyAxOS43OUwzMC45NyAxOS43OVEzMC45NyAyMC44NiAzMC4xNSAyMS40OVEyOS4zMyAyMi4xMiAyNy45MyAyMi4xMkwyNy45MyAyMi4xMlEyNy4wMSAyMi4xMiAyNi4yMyAyMS43N1EyNS40NiAyMS40MyAyNS4wMiAyMC44M1EyNC41OSAyMC4yMiAyNC41OSAxOS40MlpNNDAuODQgMjJMMzUuMjYgMjJMMzUuMjYgMTMuNDdMNDAuODAgMTMuNDdMNDAuODAgMTQuNjZMMzYuNzQgMTQuNjZMMzYuNzQgMTcuMDJMNDAuMjQgMTcuMDJMNDAuMjQgMTguMTlMMzYuNzQgMTguMTlMMzYuNzQgMjAuODJMNDAuODQgMjAuODJMNDAuODQgMjJaTTQ0LjYwIDE5LjQyTDQ0LjYwIDE5LjQyTDQ2LjA4IDE5LjQyUTQ2LjA4IDIwLjE1IDQ2LjU2IDIwLjU1UTQ3LjA0IDIwLjk1IDQ3Ljk0IDIwLjk1TDQ3Ljk0IDIwLjk1UTQ4LjcxIDIwLjk1IDQ5LjEwIDIwLjYzUTQ5LjQ5IDIwLjMyIDQ5LjQ5IDE5LjgwTDQ5LjQ5IDE5LjgwUTQ5LjQ5IDE5LjI0IDQ5LjEwIDE4Ljk0UTQ4LjcwIDE4LjYzIDQ3LjY3IDE4LjMyUTQ2LjY0IDE4LjAxIDQ2LjAzIDE3LjYzTDQ2LjAzIDE3LjYzUTQ0Ljg2IDE2LjkwIDQ0Ljg2IDE1LjcyTDQ0Ljg2IDE1LjcyUTQ0Ljg2IDE0LjY5IDQ1LjcwIDE0LjAyUTQ2LjU0IDEzLjM1IDQ3Ljg5IDEzLjM1TDQ3Ljg5IDEzLjM1UTQ4Ljc4IDEzLjM1IDQ5LjQ3IDEzLjY4UTUwLjE3IDE0LjAxIDUwLjU3IDE0LjYxUTUwLjk3IDE1LjIyIDUwLjk3IDE1Ljk2TDUwLjk3IDE1Ljk2TDQ5LjQ5IDE1Ljk2UTQ5LjQ5IDE1LjI5IDQ5LjA3IDE0LjkxUTQ4LjY1IDE0LjU0IDQ3Ljg3IDE0LjU0TDQ3Ljg3IDE0LjU0UTQ3LjE1IDE0LjU0IDQ2Ljc1IDE0Ljg1UTQ2LjM0IDE1LjE2IDQ2LjM0IDE1LjcxTDQ2LjM0IDE1LjcxUTQ2LjM0IDE2LjE4IDQ2Ljc4IDE2LjUwUTQ3LjIxIDE2LjgxIDQ4LjIxIDE3LjEwUTQ5LjIwIDE3LjQwIDQ5LjgxIDE3Ljc4UTUwLjQxIDE4LjE2IDUwLjY5IDE4LjY1UTUwLjk3IDE5LjEzIDUwLjk3IDE5Ljc5TDUwLjk3IDE5Ljc5UTUwLjk3IDIwLjg2IDUwLjE2IDIxLjQ5UTQ5LjM0IDIyLjEyIDQ3Ljk0IDIyLjEyTDQ3Ljk0IDIyLjEyUTQ3LjAxIDIyLjEyIDQ2LjI0IDIxLjc3UTQ1LjQ2IDIxLjQzIDQ1LjAzIDIwLjgzUTQ0LjYwIDIwLjIyIDQ0LjYwIDE5LjQyWiIgZmlsbD0iI0ZGRkZGRiIvPjxwYXRoIGNsYXNzPSJzdmdfX3RleHQiIGQ9Ik03OS40MyAyMkw3Ny4wOCAyMkw3Ny4wOCAxMy42MEw3OS40MyAxMy42MEw3OS40MyAxNy4wOUw4Mi42OSAxMy42MEw4NS4zMCAxMy42MEw4MS44NyAxNy4zMkw4NS40OCAyMkw4Mi43MiAyMkw4MC4zMiAxOC45NUw3OS40MyAxOS45MEw3OS40MyAyMlpNODguNzAgMjEuMzRMODguNzAgMjEuMzRMODkuNTYgMTkuNTVROTAuMDYgMTkuODggOTAuNjcgMjAuMDdROTEuMjkgMjAuMjUgOTEuOTAgMjAuMjVMOTEuOTAgMjAuMjVROTIuNTEgMjAuMjUgOTIuODcgMjAuMDJROTMuMjMgMTkuNzkgOTMuMjMgMTkuMzdMOTMuMjMgMTkuMzdROTMuMjMgMTguNTUgOTEuOTQgMTguNTVMOTEuOTQgMTguNTVMOTAuOTUgMTguNTVMOTAuOTUgMTcuMDVMOTIuNDUgMTUuNDRMODkuMTQgMTUuNDRMODkuMTQgMTMuNjBMOTUuMjEgMTMuNjBMOTUuMjEgMTUuMDlMOTMuNDcgMTYuOTZROTQuNTEgMTcuMTggOTUuMDcgMTcuODJROTUuNjMgMTguNDYgOTUuNjMgMTkuMzdMOTUuNjMgMTkuMzdROTUuNjMgMjAuMTEgOTUuMjIgMjAuNzVROTQuODIgMjEuMzkgOTQuMDAgMjEuNzhROTMuMTggMjIuMTcgOTEuOTcgMjIuMTdMOTEuOTcgMjIuMTdROTEuMDggMjIuMTcgOTAuMjEgMjEuOTVRODkuMzQgMjEuNzQgODguNzAgMjEuMzRaTTk5LjcyIDIxLjI0TDk5LjcyIDIxLjI0TDEwMC41MCAxOS40OVExMDEuMDYgMTkuODYgMTAxLjgwIDIwLjA5UTEwMi41NSAyMC4zMiAxMDMuMjcgMjAuMzJMMTAzLjI3IDIwLjMyUTEwNC42MyAyMC4zMiAxMDQuNjQgMTkuNjRMMTA0LjY0IDE5LjY0UTEwNC42NCAxOS4yOCAxMDQuMjUgMTkuMTFRMTAzLjg2IDE4LjkzIDEwMi45OSAxOC43NEwxMDIuOTkgMTguNzRRMTAyLjA0IDE4LjUzIDEwMS40MSAxOC4zMFExMDAuNzcgMTguMDYgMTAwLjMyIDE3LjU1UTk5Ljg2IDE3LjAzIDk5Ljg2IDE2LjE2TDk5Ljg2IDE2LjE2UTk5Ljg2IDE1LjM5IDEwMC4yOCAxNC43N1ExMDAuNzAgMTQuMTUgMTAxLjU0IDEzLjc5UTEwMi4zNyAxMy40MyAxMDMuNTggMTMuNDNMMTAzLjU4IDEzLjQzUTEwNC40MSAxMy40MyAxMDUuMjEgMTMuNjJRMTA2LjAyIDEzLjgwIDEwNi42MyAxNC4xN0wxMDYuNjMgMTQuMTdMMTA1LjkwIDE1LjkzUTEwNC43MCAxNS4yOCAxMDMuNTcgMTUuMjhMMTAzLjU3IDE1LjI4UTEwMi44NiAxNS4yOCAxMDIuNTQgMTUuNDlRMTAyLjIxIDE1LjcwIDEwMi4yMSAxNi4wNEwxMDIuMjEgMTYuMDRRMTAyLjIxIDE2LjM3IDEwMi42MCAxNi41NFExMDIuOTggMTYuNzEgMTAzLjgzIDE2Ljg5TDEwMy44MyAxNi44OVExMDQuNzkgMTcuMTAgMTA1LjQyIDE3LjMzUTEwNi4wNSAxNy41NiAxMDYuNTIgMTguMDdRMTA2Ljk4IDE4LjU4IDEwNi45OCAxOS40NkwxMDYuOTggMTkuNDZRMTA2Ljk4IDIwLjIxIDEwNi41NiAyMC44M1ExMDYuMTQgMjEuNDQgMTA1LjMwIDIxLjgwUTEwNC40NiAyMi4xNyAxMDMuMjYgMjIuMTdMMTAzLjI2IDIyLjE3UTEwMi4yNCAyMi4xNyAxMDEuMjggMjEuOTJRMTAwLjMyIDIxLjY3IDk5LjcyIDIxLjI0WiIgZmlsbD0iI0ZGRkZGRiIgeD0iNzUuODkiLz48L3N2Zz4=)](https://forthebadge.com)

This repository contains all the files used to create the cluster. This's composed of raspberry pi 3, which run the Linux os Debian distribution without graphical interface.

<hr/>

Este repositório contém todos os arquivos utilizados para a criação do cluster em questão. Esse é composto por raspberry pi 3, os quais executam o sistema operacional Linux distribuição Debian sem inferface gráfica. 
