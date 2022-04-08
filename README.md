# Fuel Rats

## Concept

All vehicles are spawned at the same time. A single `canister` and a `goal` are created during a round. During a round the `canister` must be taken to the `goal`. The `canister` can be stolen from the `canister` holder by bumping the front of your vehicle into the `canister holder`.

Upon bringing the `canister` to the goal a point is given to the player and a new round will begin.

## Scope
```
- Select Car Color, Neon, etc.
- 1 Car Type Randomly Per Matchup
- Include Boost + Jumping
- Discord Auth through Ares
- All cars have no max speed, except ball holder
- Ball holder is always at least 10 speed units slower if not more
- Ball holder gets slower over time
- Hidden power up that changes goal position once per round
- Maximum Players - 24~
```

## Folder Structure
```text
📂 src            # Where the code lives
├── 📂 client         # Client-side
├── 📂 configs        # Folders with 'resource.cfg'
├── 📂 core           # Shared code (event names, etc)
├── 📂 mods           # MLOs, Vehicles, etc.
├── 📂 server         # Server-side
├── 📂 webview        # UI / WebView
└── 📂 utility        # Scripts that assist with the build pipeline
```

_Do not put anything in the `resources` folder. It will be overwritten._

## Installation

```
npm install -g yarn
```

```
yarn install
```

```
yarn update
```

## Configurations

**First, never ever modidfy server.cfg. Changes will not be saved.**

All configurations are under the `config` folder.

Modify each environment configuration accordingly.

## Running

When running this repository it will automatically build on files based on repository.

_Develop alone with `yarn dev`. Test with friends with `yarn devtest`. Deploy with `yarn linux` or `yarn windows`_

| OS      | Description                  | Command        |
| ------- | ---------------------------- | -------------- |
| Linux   | WebView Build + Mods         | `yarn linux`   |
| Windows | WebView Build + Mods         | `yarn windows` |
| Windows | WebView Build + Mods + Debug | `yarn devtest` |
| Windows | Mods + Debug                 | `yarn dev`     |