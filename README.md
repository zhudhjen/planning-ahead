# RhythmJump
A music based platform game

## Docs

- Chinese GDD: [Google Docs](https://docs.google.com/document/d/1o8JgMRD53AjWpdXvaA8AGeciMkFDwY28pzybJHmWqKY/edit)
- English GDD: [Google Docs](https://docs.google.com/document/d/1kXH58Myj2T4DLfro5Uc1xLvNs8SQxa3L3cDC9CGhSiI/edit)

## Development

References:

- Basic Git operations: [The Tutorial](https://git-scm.com/docs/gittutorial) (Only the basics are required)

- Use Git with UE4 projects: [Unreal Wiki](https://wiki.unrealengine.com/Git_source_control_(Tutorial)) (Important steps are described below)

### Get Started

1. [Git LFS](https://git-lfs.github.com/) is used to track binary files in this repo, install it first: [Guide](https://help.github.com/articles/installing-git-large-file-storage)

2. Clone the repo:

   ```
   git clone https://github.com/zhudhjen/RhythmJump.git
   ```

3. Track binary file types with Git LFS (extend it if more binary types are introduced, e.g. mp3/jpg/png):

   ```shell
   git lfs install
   git lfs track "*.uasset"
   git lfs track "*.umap"
   git lfs track "*.wav"
   ```

4. You may now perform normal git operations on this repo.

### Configure Unreal Editor (Optional)

The [UE4 Git Source Control Plugin](https://github.com/SRombauts/UE4GitPlugin) is used in the UE4 Editor to manage git.

1. Open the UE4 project `RhythmJump.uproject`.
2. The first time you open the project, there may be a prompt tells you that you need to recompile the plugin to continue, click yes. Wait until the compilation finish and the project will automatically launch. 
   - Compilation succeeded with UE4.21.2 and macOS 10.13.6 
3. Open `Source Control` in toolbar and select `Change Source Control Settings ...`.
4. In the pop-up window, switch the provider to `Git LFS 2` and confirm the path of git executable is correctly filled in `Git Path` .
5. Select `Accept Settings` .
6. You can now add/submit(commit)/pull/push files in UE4 Editor. 

### Notes

- As an alternative to the native git command line tool, the [GitHub Desktop](https://desktop.github.com/) can be used as a GUI tool if you prefer. Note that you may still need to use the native command line tool to complete configuring Git LFS. 
- Default `.gitignore` file is used, provided by GitHub. Modify it if needed.
- Whatever method you are using, remember to perform `git pull`  before start working to avoid merge conflicts. Also, try to communicate with the team when you are going to make a change,  pull/commit/push frequently and make everyone happy.

## Contributors

- Peifeng Ye

- Dinghan Zhu

- Qiming Du
- Junrui Zhao
- Chuanzhe Li