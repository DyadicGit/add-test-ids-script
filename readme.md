# This tool adds data-test-id's to react files (jsx, tsx)
### How to use:
1) do `npm i`
2)  * run it using `npm run start` or just `node add-test-ids.js`
    * run using custom a directory `npm run start io-dir=../my/react-app`
    * assigning test-id's to all html tags 
`npm run start io-dir=../my/react-app --all`
    * overriding the default `data-test-id` attribute 
      `npm run start io-dir=../my/react-app --all customAttribute=test-id`
    * or you can copy-paste a `.jsx/.tsx` file to `/input` folder, then do `npm run start` 

___

Of course, you can also change variables `INPUT_FOLDER`, `OUTPUT_FOLDER` to point to your input & output destination
(files can be overridden, so the input & output paths can be the same)

  

#### Example:
>example file before: [input/exampleApp.component.tsx](input/exampleApp.component.tsx)
>
> do `npm run start`
>
>example file after: [output/exampleApp.component.tsx](output/exampleApp.component.tsx)

___

##### To what HTML elements test-id's are assigned?
Script has three lists of html elements/tags, described in [this file](transforms/constants.js): 
* custom list of your joice `MY_TAGS` - picked by default
* all HTML tags `HTML_TAGS` - picked when running with `--all` flag
* MUI library tags `MUI_TAGS` - added to the list when running with `--mui` flag
