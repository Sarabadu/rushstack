## API Report File for "@rushstack/package-extractor"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { IPackageJson } from '@rushstack/node-core-library';
import { ITerminal } from '@rushstack/terminal';

// @public
export interface IExtractorDependencyConfiguration {
    dependencyName: string;
    dependencyVersionRange: string;
    patternsToExclude?: string[];
    patternsToInclude?: string[];
}

// @public
export interface IExtractorMetadataJson {
    links: ILinkInfo[];
    mainProjectName: string;
    projects: IProjectInfoJson[];
}

// @public
export interface IExtractorOptions {
    createArchiveFilePath?: string;
    createArchiveOnly?: boolean;
    dependencyConfigurations?: IExtractorDependencyConfiguration[];
    folderToCopy?: string;
    includeDevDependencies?: boolean;
    includeNpmIgnoreFiles?: boolean;
    linkCreation?: 'default' | 'script' | 'none';
    mainProjectName: string;
    overwriteExisting: boolean;
    pnpmInstallFolder?: string;
    projectConfigurations: IExtractorProjectConfiguration[];
    sourceRootFolder: string;
    targetRootFolder: string;
    terminal: ITerminal;
    transformPackageJson?: (packageJson: IPackageJson) => IPackageJson | undefined;
}

// @public
export interface IExtractorProjectConfiguration {
    additionalDependenciesToInclude?: string[];
    additionalProjectsToInclude?: string[];
    dependenciesToExclude?: string[];
    patternsToExclude?: string[];
    patternsToInclude?: string[];
    projectFolder: string;
    projectName: string;
}

// @public
export interface ILinkInfo {
    kind: 'fileLink' | 'folderLink';
    linkPath: string;
    targetPath: string;
}

// @public
export interface IProjectInfoJson {
    path: string;
    projectName: string;
}

// @public
export class PackageExtractor {
    extractAsync(options: IExtractorOptions): Promise<void>;
    // @beta
    static getPackageIncludedFilesAsync(packageRootPath: string): Promise<string[]>;
}

// (No @packageDocumentation comment for this package)

```