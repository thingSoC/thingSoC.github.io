# thingSoC.github.io
=====================

thingSoC.github.io - System on Chip Platform for the Internet of Things - Organization Website
moxondesign.github.io


thingSoC Organization Website

This is the source of the thingSoC website [http://thingSoC.com/](http://thingSoC.com)

The only interesting branch in this repo will be the *source* branch;
as GitHub expects the generated website to live in the *master* branch.

The website is built using the Jekyll blogging tools (native to Github pages) 
and the Zurb Foundation framework for a responsive layout system.

See the github pages documentation for installation directions:
[https://help.github.com/articles/using-jekyll-with-pages/] (using-jekyll-with-pages)

To use Ruby/Jekyll to build the website:
> rake generate

To test the website locally (at http://127.0.0.1:4000) :
> jekyyl serve

To publish (push) the website back to Github:

* Make changes in the *source* branch
* Build and test the site locally
* Commit changes to *source* branch
* `git publish-website` which consists of the following steps
  - `git branch -D master`
  - `git checkout -b master`
  - `git filter-branch --subdirectory-filter site/ -f`
  - `git merge source` *first time through*
  - `git checkout source`
  - `git push --all origin`

THIS SOFTWARE IS PROVIDED BY THE CONTRIBUTORS "AS IS" AND WITHOUT ANY EXPRESS OR IMPLIED WARRANTIES,
INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED.
IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY,
OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA,
OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
