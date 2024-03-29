Abstractive has been discontinued as of 27/2/2023.

# Abstractive Mods

If you have a Fortnite mod you've created and would like it on the Abstractive marketplace you can create a pull request after reading the terms and creating a config file with the following schema.

## Terms

**Only mods YOU have created are allowed on Abstractive**, if you believe your work has been incorrectly uploaded, please contact me directly via [email](mailto:jacksta@pm.me). The first version must be versioned according to the semantic versioning specification, learn more [here](https://semver.org). While your mod **does not** have to be open-source each version will require a full audit by a trusted, direct contributor to Abstractive. If your mod is open-source, you will be able to access the repository directly from within Abstractive, and your mod (and future updates) are released quicker. We retain the right to refuse any new or existing mod from being available at anytime without reasoning, however if applicable changes need to be made we will let you know. Harmful, malicious or insensitive content is forbidden at all times and will not be accepted. We are not responsible for malicious content that may appear on Abstractive, in the case that it does, we will take corrective action upon discovery and make users of said content aware by email, client and/or announcement on Twitter.

**Using functions of Abstractive you agree to these terms (including adding mods to this repository).**

## Getting started

You can add a mod by forking & cloning this repository. Create a folder in `mods` with your modderID. Within that folder, add a folder with the id of your mod (this has to be the id in your info.json) - this is the 'root directory' of your mod. And another folder inside the root directory with the version of your mod you are uploading. Make a `info.json` file using the schema, examples and templates below, place this in the root directory. Within your 'version' folder add your paks and signature files. Check here for my example using [SkinsUniversal](https://github.com/jwhazy/abstractive-mods/tree/main/mods/214598871513432064/) - note that this isn't a real mod.

## Examples & Templates

You can see examples and templates in the GitHub repository under `example\configs` in their respective folders. An template is a JSON file with the keys and no values. An example is the same except with placeholder information. Use these to create your own info.json.

## Issues or feedback?

Issues can be directly resolved with me inside the [Jacksta Development Discord server](https://discord.gg/jvaBE3vVBe). Any feedback or changes you believe would benefit Abstractive can be requested also inside the Discord, or fixed with a PR.

## Schema

### Required fields

`id` (string): A custom identifer, this can only contain letters. This has to match the name of the folder. No longer than 24 characters.

`name` (string): The name of your mod, keep this short if possible.

`shortDescription` (string): A shorter version of your description, think of this like a blurb.

`currentVersion` (string): This is the latest version downloadable. **This has to be versioned correctly or your PR will be rejected**.

`previousVersion` (string[]): This is the latest version downloadable. **This has to be versioned correctly or your PR will be rejected**. Make this empty if this is a new mod.

`clients` (Version[] | string[]): All clients that support your mod. **You need to test that your mod works on these versions**. You can find a list of versions supported by Abstractive [here]().

`content` (object):

```
icon (string): URL to icon - upload on imgur or another service.
banner (string): URL to banner - upload to imgur or another service.
```

`files` (object[]):

```
file (string): Name of the file in the repository - include file extension.
type ("Pak" | "Sig" | "Other"): Type of file in the repository.
includesSig (boolean): If you include a signature file make this false.
```

### Optional fields

Extending on top of the required fields.

`longDescription` (string): This is a description of your mod if you need it.

`contributors` (string[]): If you need to credit others put their name here, do not put modderIDs or links here.

`repository` (string): If your mod is open-source put the GitHub repository link here.

`content` (object):

```
primaryColor (string): A primary color in hex code.
primaryColor (string): A secondary color in hex code.
media (string[]): Screenshots (URLs) of your mod.
```
