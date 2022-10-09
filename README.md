# Optifine Utils

> A scraper to get a information about and download jar files from <a href="https://optifine.net">optifine.net</a>

## Install

```bash
npm install optifine-utils
```

or

```bash
yarn add optifine-utils
```

## Quick Start

```ts
import OFUtils from 'optifine-utils';

const version = await (
    await OFUtils.getVersions({ minecraftVersion: '1.19.2' })
)[0];

version.download('./Optifine_1.19.2.jar');
```

## Docs

### Types

#### Version

```ts
type Version = {
    optifineVersion: string;
    fileName: string;
    forgeVersion: string;
    minecraftVersion: string;
    published: Date;
    changelogURL: string;
    download?: (path?: string) => Promise<void>;
    getDownloadURL: () => Promise<string>;
};
```

#### GetVersionsFilter

```ts
type GetVersionsFiler = {
    optifineVersion?: string;
    fileName?: string;
    forgeVersion?: string;
    minecraftVersion?: string;
    published?: Date;
    changelogURL?: string;
};
```

### Methods

#### getDownloadURL

```ts
getDownloadURL(fileName: string): Promise<String>
```

#### getVersions

```ts
getVersions(filter?: GetVersionsFilter): Promise<Version[]>
```

#### downloadVersion

```ts
getVersions(version: Version, path: string): Promise<void>
```

## Credits

All Development is by ([@teakivy](https://www.github.com/teakivy))

## Support

For support, Join my discord ([dsc.gg/teakivy](https://discord.gg/Xb6eeRevkb)) and ask for help in `#❓︱support`
