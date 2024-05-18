# action-get-datetime

Simple action that names datetimes more useful in github actions.

![Tests Status](https://img.shields.io/github/actions/workflow/status/benzine-framework/action-get-datetime/test.yml?logo=github&label=Tests)
![QC Status](https://img.shields.io/github/actions/workflow/status/benzine-framework/action-get-datetime/trunk.check.yml?logo=github&label=QC)

## Usage

Use it like so:

```yaml
- uses: benzine-framework/action-get-datetime@v1
  id: get-datetime
- run: echo "The current datetime is ${{ steps.get-datetime.outputs.datetime }}"
```

or

```yaml
- uses: benzine-framework/action-get-datetime@v1
- run: echo "The current datetime is ${{ env.DATETIME }}"
```

## Outputs

| Output                                | Env                    | Description                                                |
| ------------------------------------- | ---------------------- | ---------------------------------------------------------- |
| `steps.date.outputs.datetime`         | `env.DATETIME`         | The current datetime in the format `YYYY-MM-DDTHH:MM:SSZ`. |
| `steps.date.outputs.date`             | `env.DATE`             | The current date in the format `YYYY-MM-DD`.               |
| `steps.date.outputs.time`             | `env.TIME`             | The current time in the format `HH:MM:SS`.                 |
| `steps.date.outputs.atom`             | `env.ATOM`             | The current datetime in ATOM format.                       |
| `steps.date.outputs.atom_with_millis` | `env.ATOM_WITH_MILLIS` | The current datetime in ATOM format with milliseconds.     |
