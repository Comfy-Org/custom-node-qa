# ComfyUI Custom Node QA

Tools for batch testing custom nodes on ComfyUI Cloud.

## Scripts

`scripts/devtools-node-pack-tester.js` - copy/paste into browser devtools console:

```js
// 1. Open ComfyUI in browser
// 2. Open devtools (F12)
// 3. Paste entire script contents into console
// 4. Run commands:

await QA.listPacks() // list all packs
await QA.checklist() // download markdown checklist
await QA.testPack('comfyui-impact-pack') // clear, add all nodes, save
await QA.testAllPacks() // test every pack
QA.help() // full command list
```

## Structure

- `scripts/` - devtools scripts (paste into browser console)
- `workflows/` - saved workflow files (`all-nodes-{pack}.json`)
- `checklists/` - generated QA checklists

## Development

```sh
npm install
npm run format        # format all files
npm run format:check  # check formatting
npm run validate:json # validate workflow files
```
