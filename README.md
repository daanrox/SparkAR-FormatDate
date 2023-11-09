# SparkFormatDate
> Script de patch para formatação de data para Spark AR Studio.

![Screenshot](./screenshot.jpg)


## Usage
Abaixo estão as inputs/outputs de patch que você deve definir para o script.

### From Script

#### `date`
* **Description**: Data formatada que você recebe do script.
* **Type**: Text

### To Script

#### `format`
* **Description**: Defina em qual padrão de formato o texto da data será gerado.
* **Type**: Text
* **Optional**: `true`
* **Default**: `'YYYY-MM-DD HH:mm:ss'`

**Patterns**
| Input | Example | Description
| --- | --- | ---
| `YYYY` | `2021` | 4 digit year.
| `YY` | `21` | 2 digit year.
| `MM` | `02` | Month number from 01 to 12 (with leading zero).
| `M` | `2` | Month number from 1 to 12.
| `DD` | `09` | Day of month from 01 to 31 (with leading zero).
| `D` | `9` | Day of month from 1 to 31.
| `HH` | `06` | Hours (24 hour time) from 00 to 23 (with leading zero).
| `H` | `6` | Hours (24 hour time) from 0 to 23.
| `hh` | `03` | Hours (12 hour time) from 01 to 12 (with leading zero).
| `h` | `3` | Hours (12 hour time) from 1 to 12.
| `mm` | `04` | Minutes from 00 to 59 (with leading zero).
| `m` | `4` | Minutes from 0 to 59.
| `ss` | `07` | Seconds from 00 to 59 (with leading zero).
| `s` | `7` | Seconds from 0 to 59.
| `A` | `PM` | Post or ante meridiem in uppercase.
| `a` | `am` | Post or ante meridiem in lowercase.

#### `refreshInterval`
* **Description**: Intervalo em segundos em que o texto da data será atualizado.
* **Type**: Number
* **Optional**: `true`
* **Default**: `1`

#### `debug`
* **Description**: Exibir mensagens de depuração no console.
* **Type**: Boolean
* **Optional**: `true`
* **Default**: `false`

## Credits
* [Josh Beckwith](https://github.com/positlabs) for making [spark-localtime](https://github.com/positlabs/spark-localtime), which inspired me to create this script. I originally planned to contribute to his repo, but since his script relied on the `toLocaleDateString` method and it doesn't seen to work on Spark AR Studio anymore, I just made my own script from scratch;
* [Daanrox](https://www.instagram.com/daanrox/) (https://daanrox.com/) for creating Instagram filters, which made me see the limitations of Spark AR Studio in relation to date formats and inspired me to help her.
