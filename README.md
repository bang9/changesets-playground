# changesets-playground


## .changeset/config.json

### options
https://github.com/changesets/changesets/blob/main/docs/config-file-options.md

### custom commit message

Use default generator

```json
{
  commit: true
}
```

Use custom generator

```json
{
  commit: ['./scripts/commit.js', { customOption: true }]
}
```

```ts
// scripts/commit.js

// type VersionType = 'major' | 'minor' | 'patch';
// type Release = {
//   name: string;
//   type: VersionType;
// }
// type Changeset = {
//   summary: string;
//   releases: Array<Release>;
// }
async function getAddMessage(changeset: Changeset, commitOptions: any): Promise<string> {
}

// type NewChangeset = Changeset & {
//   id: string;
// };
// type ComprehensiveRelease = {
//   name: string;
//   type: VersionType;
//   oldVersion: string;
//   newVersion: string;
//   changesets: string[];
// };
// type ReleasePlan = {
//   changesets: NewChangeset[];
//   releases: ComprehensiveRelease[];
//   preState: PreState | undefined;
// };
async function getVersionMessage(releasePlan: ReleasePlan, commitOptions: any): Promise<string> {

}

module.exports = {
  getAddMessage,
  getVersionMessage
}
```
