# ComfyUI SUPIR upscaler wrapper node

## WORK IN PROGRESS

# Installing
Either manager and install from git, or clone this repo to custom_nodes and run:

`pip install -r requirements.txt`

or if you use portable (run this in ComfyUI_windows_portable -folder):

`python_embeded\python.exe -m pip install -r ComfyUI\custom_nodes\ComfyUI-SUPIR\requirements.txt`

Additionally xformers might be necessary.

Get the SUPIR model(s) from the original links below, they are loaded from the normal ComfyUI/models/checkpoints -folder
In addition you need an SDXL model, they are loaded from the same folder.

## WARNING: currently downloads 10GB clip model as I didn't figure out a way to use existing ones yet

# Tests
Video upscale test (currently the node does frames one by one from input batch):

Original: https://github.com/kijai/ComfyUI-SUPIR/assets/40791699/33621520-a429-4155-aa3a-ac5cd15bda56

Upscaled 3x: https://github.com/kijai/ComfyUI-SUPIR/assets/40791699/d6c60e0a-11c3-496d-82c6-a724758a131a

Image upscale from 3x from 512p:
https://github.com/kijai/ComfyUI-SUPIR/assets/40791699/545ddce4-8324-45cb-a545-6d1f527d8750



-------------------------------------------


Original repo:
https://github.com/Fanghua-Yu/SUPIR

#### Models we provided:
* `SUPIR-v0Q`: [Baidu Netdisk](https://pan.baidu.com/s/1lnefCZhBTeDWijqbj1jIyw?pwd=pjq6), [Google Drive](https://drive.google.com/drive/folders/1yELzm5SvAi9e7kPcO_jPp2XkTs4vK6aR?usp=sharing)
    
    Default training settings with paper. High generalization and high image quality in most cases.

* `SUPIR-v0F`: [Baidu Netdisk](https://pan.baidu.com/s/1AECN8NjiVuE3hvO8o-Ua6A?pwd=k2uz), [Google Drive](https://drive.google.com/drive/folders/1yELzm5SvAi9e7kPcO_jPp2XkTs4vK6aR?usp=sharing)

    Training with light degradation settings. Stage1 encoder of `SUPIR-v0F` remains more details when facing light degradations.


## BibTeX
    @misc{yu2024scaling,
      title={Scaling Up to Excellence: Practicing Model Scaling for Photo-Realistic Image Restoration In the Wild}, 
      author={Fanghua Yu and Jinjin Gu and Zheyuan Li and Jinfan Hu and Xiangtao Kong and Xintao Wang and Jingwen He and Yu Qiao and Chao Dong},
      year={2024},
      eprint={2401.13627},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
    }

---

## 📧 Contact
If you have any question, please email `fanghuayu96@gmail.com`.

---
## Non-Commercial Use Only Declaration
The SUPIR ("Software") is made available for use, reproduction, and distribution strictly for non-commercial purposes. For the purposes of this declaration, "non-commercial" is defined as not primarily intended for or directed towards commercial advantage or monetary compensation.

By using, reproducing, or distributing the Software, you agree to abide by this restriction and not to use the Software for any commercial purposes without obtaining prior written permission from Dr. Jinjin Gu.

This declaration does not in any way limit the rights under any open source license that may apply to the Software; it solely adds a condition that the Software shall not be used for commercial purposes.

IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

For inquiries or to obtain permission for commercial use, please contact Dr. Jinjin Gu (hellojasongt@gmail.com).
