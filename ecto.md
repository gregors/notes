# Ecto

## Generate a Rep

```bash
mix ecto.gen.repo -r Boom.Repo
```

## actually create the db

```bash
mix ecto.create
```

## add a migration

```bash
mix ecto.gen.migration create_my_awesome_thing
```

Ends up in `priv/repo/migrations`

## Example Migration
```elixir
defmodule Animals.Repo.Migrations.CreateDogs do
  use Ecto.Migration

  def change do
    create table(:dogs) do
      add(:name, :string)
      add(:age, :integer)
    end
  end
end
```

## run migration

```bash
mix ecto.migrate
```

```bash
mix ecto.gen.migration create_my_awesome_thing
```

## Example Schema
usually in lib/animals

```elixir
defmodule Animals.Dog do
  use Ecto.Schema

  schema "dogs" do
    field(:name, :string, null: false)
    field(:age, :integer)
  end
end
```

## Example Changeset

```elixir
defmodule Animals.Dog do
  use Ecto.Schema

  schema "dogs" do
    field(:name, :string, null: false)
    field(:age, :integer)
  end

  def changeset(dog, \\ %{}) do
    dog
    |> Ecto.Changeset.cast(params, [:name, :age])
    |> Ecto.Changeset.validate_required([:name])
  end
end
```

## Example operations

### Insert
```elixir
%Animals.Dog{name: "Peppers", 5} |> Animals.Repo.insert
```

### Count
```elixir
Trains.Repo.aggregate(Dog, :count)
```

### Query

```elixir
require Ecto.Query
Ecto.query(Dog, name: "Peppers") |> Animals.Repo.all
```
