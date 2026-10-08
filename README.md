# Horizon Calc

Horizon Calc is a spreadsheet with a 4D spin. Your sheets sit at places in three dimensions you choose (products × markets × scenarios, stores × regions, projects × phases × teams…) and their numbers change over time. You see them as a 3D grid of cells whose blocks grow and shrink as the timeline plays, and as ordinary Excel-sized sheets with formulas. Start from a template (a business case, a factory, a retail network, a project portfolio, or one of four tax and legal examples) or a blank document. Every example also comes with a lively animation of its own numbers, and if you like, an AI helps draft dimensions and sheets, or builds a small app on top of your cells. It belongs to the Horizon suite, next to [Horizon](https://github.com/BartJanCoppens/Horizon) for presentations.

It works on **Mac**, **Windows** and **Linux**. It's free and needs no account.

**[⬇ Download the latest version](https://github.com/BartJanCoppens/Horizon-Calc-Releases/releases/latest)**

---

## 1. Download

Open the [latest release](https://github.com/BartJanCoppens/Horizon-Calc-Releases/releases/latest), scroll down to **Assets** and click the file for your computer:

| Your computer | File to download |
|---|---|
| Mac with an Apple chip (M1, M2, M3, M4…) | `Horizon-Calc-<version>-arm64.dmg` |
| Mac with an Intel processor | `Horizon-Calc-<version>-x64.dmg` |
| Windows 10 or 11 | `Horizon-Calc-Setup-<version>-x64.exe` |
| Linux (most distributions) | `Horizon-Calc-<version>-x86_64.AppImage` |
| Linux (Ubuntu, Debian and similar, as a package) | `Horizon-Calc-<version>-amd64.deb` |

Not sure which Mac you have? Click the Apple menu  › **About This Mac**. If it says **Chip: Apple M…**, take the Apple chip file; if it says **Processor: Intel**, take the Intel file.

You can ignore the other files (`.zip`, `.blockmap`, `.yml`): the app uses them for its updates.

## 2. Install

Horizon Calc is made by one person for friends and family, so it isn't registered with Apple or Microsoft. Your computer will therefore warn you the first time you open it. That's expected; the steps below show how to get past the warning once.

### Mac

1. Open the `.dmg` file you downloaded.
2. Drag **Horizon Calc** onto the **Applications** folder in the window that appears.
3. Open **Horizon Calc** from your Applications folder (or with Spotlight).
4. macOS says it can't check Horizon Calc for malicious software and won't open it. Click **Done** (or **OK**).
5. Open **System Settings** › **Privacy & Security**, scroll down to the message about Horizon Calc and click **Open Anyway**. Confirm with your password or Touch ID, then click **Open Anyway** once more.

From then on Horizon Calc opens normally. Needs macOS 12 (Monterey) or later.

### Windows

1. Double-click `Horizon-Calc-Setup-<version>-x64.exe`.
2. If Windows shows **Windows protected your PC**, click **More info**, then **Run anyway**.
3. Horizon Calc installs by itself (no administrator rights needed) and opens. You'll find it in the Start menu afterwards.

Needs Windows 10 or 11, 64-bit.

### Linux

**AppImage** (works on most distributions):

```sh
chmod +x Horizon-Calc-*-x86_64.AppImage
./Horizon-Calc-*-x86_64.AppImage
```

Or right-click the file › **Properties** › **Permissions**, tick **Allow executing file as program**, then double-click it. On Ubuntu 22.04 or later, if it doesn't start, install FUSE first: `sudo apt install libfuse2` (on Ubuntu 24.04: `sudo apt install libfuse2t64`).

**Debian package:**

```sh
sudo apt install ./Horizon-Calc-*-amd64.deb
```

Horizon Calc then appears in your applications menu.

## 3. Getting started

The first time, Horizon Calc asks you to pick a template: **Blank**, **Factory**, **Business case**, **Retail network** or **Project portfolio**, or one of the tax and legal examples: **Pillar Two** (the 15% global minimum tax), **Holding structure**, **Claims and litigation** and **Advisory firm**. Each opens with its dimensions, sheets, formulas and a timeline you can play. The figures in the examples are made up to show how it works: replace them with your own, and don't take them as tax or legal advice.

Along the top is a menu bar, as in Excel: **File**, **Edit**, **Insert**, **Format**, **Formulas**, **Data**, **View** and **Examples** (to add another example next to your documents). The usual shortcuts work: copy and paste (also to and from Excel), undo and redo, fill down, find and replace, inserting rows and columns. The **Formulas** menu lists every function with an example, including Excel's own `SUMIFS`, `COUNTIF`, `SUMPRODUCT`, `ROUNDUP`, `IFS`, `NPV`, `IRR` and `PMT`. Type numbers the way you write them: 1,250.50 or 1.250,50, 15% or €1.250, as in Excel. Double-click the edge of a column letter to fit the column to its text, and use **Format › Plain number** to show years as 2026 rather than 2,026. **Insert › Chart** draws the cells you selected as a chart that moves with the timeline. To note where a table's figures come from, select it and click **Add source**: one source covers every number in it. **Data › Goal Seek…** finds the value of an input that makes a formula reach a target ("the royalty rate that brings the effective rate to 15%"), and beside the selected cell's value a small line shows it over time: click it to jump to that period.

### Where the figures come from

Every input has a small dot: amber when it has no source, violet when the figure is made up as an example (illustrative: all the examples' figures are), green once a source backs it. Click the source text in the status bar to open the input's card. There you can quote a passage from a source, say it's your own figure and what it rests on, or **Check with AI**. Statements you write about the numbers ("The site is cash-positive by M18") get the same treatment. **Sources…** keeps a document's web pages, documents (PDF, text, Markdown, CSV, TSV or JSON, kept on your computer) and notes of your own, and **All documents** finds a source you used elsewhere. From there, save a **Report** of every figure and what backs it as a web page, the sources as **Citations** (BibTeX) or a **Spreadsheet**.

Above the 3D grid you can switch to the example's **animation** (✦), which plays along with the timeline. When the grid gets crowded, hide a sheet with the ✕ on its label (**Show all** brings them back), or show only the totals, or only the sheet you're working on and the ones it uses, with the **Labels** box. A document with many sheets starts by labelling only its totals; your choice is kept with the document.

Your documents are kept on your computer, in the app.

## 4. Connect an AI (optional)

You can use everything without AI. With it, the AI drafts sheets and dimensions from a sentence, builds a small **app** on cells you select (**Insert › App from selection…**), and makes **animations** of your numbers (**Insert › Animation from selection…**): you describe how it should look and what it should do, and keep chatting to change it.

Horizon Calc is made and tested with Claude, and also works with OpenAI, Gemini, OpenRouter, Mistral, Groq, DeepSeek, or models you run yourself with Ollama or LM Studio (no key; on this computer, nothing leaves it). To connect one:

1. Open **File › Models & keys…**. Next to a provider, **Get a key** opens its page: for Claude, sign up at [console.anthropic.com](https://console.anthropic.com), add some credit under **Billing**, and create a key under **API keys**. You pay the provider for what you use.
2. Click **Add key…**, paste the key and click **Save**. **Test** checks it and lets you choose one of its models.

Keys are stored encrypted by your computer's keychain and only ever sent to their own provider. The AI is told your sheets' labels and formats, never their numbers, with one exception: **Check with AI** sends the figures and statements you chose to check, with your sources (documents included). The first time in a document, it asks whether it may also search the web (with Claude only). Without a model, the AI panel makes simpler drafts by itself, and apps and animations start from simple built-in designs.

### Share your work

- **An Excel file**: **File › Export to Excel…** saves the document as an `.xlsx` workbook for someone with only Excel: an Overview (the dimensions, every sheet, a picture of the animation), a worksheet for each sheet with a column for each period and live formulas (change an input and every later period follows), the statements and the sources. Your own documents go in by title only.
- **An app as a file**: under an app, **Export…** saves it as one HTML file that opens in any browser, offline, with only the cells it needs (you see which sheets before saving). Changes there are what-ifs and are never saved. Its **Sources** panel shows what backs its inputs, naming only web pages: your own documents are never named or quoted.
- **An animation**: **Export…** on an animation saves it for a [Horizon](https://github.com/BartJanCoppens/Horizon) presentation (it plays live on the slide), as an MP4 video, or as a PowerPoint slide with the video.
- **A slide**: **Insert as slide › PowerPoint…** saves the slide frame as a PowerPoint slide, with the sheet as a table or the rows as a chart. Its speaker notes list the sheet's figures and their sources.

Apps and animations run walled off from the rest of Horizon Calc: they can't see your other documents or your key, and can't reach the internet. Changing a number in an app changes nothing in your sheet until you click **Apply to model**.

## Updates

- **Windows** and **Linux AppImage**: new versions download in the background and install the next time you restart Horizon Calc.
- **Mac** and **Linux .deb**: Horizon Calc tells you when a new version is ready, with a **Download** button. Install it the same way as the first time.

## Uninstall

- **Mac**: drag **Horizon Calc** from Applications to the Bin.
- **Windows**: **Settings › Apps › Installed apps**, find Horizon Calc › **Uninstall**.
- **Linux**: delete the AppImage, or run `sudo apt remove horizon-calc`.

## Questions or problems

Contact Bart Jan directly, or [open an issue](https://github.com/BartJanCoppens/Horizon-Calc-Releases/issues) here.
