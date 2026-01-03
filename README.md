# openmind-developer-guide
How to claim the developer badge on openmind with little to no dev knowledge


openmind developer badge

a detailed guide to contribute and earn the badge

what is needed:
  - octaspace
  - openmind OM1 api key
  - patience
  - $1 in octa and $2 credit for api

step 1:
> rent machine from octaspace market place
  - visit: marketplace.octa.computer/compute
  - sign in
  - you can fund your octaspace with OCTA token from mexc (10 OCTA tokens is enough)
  - go to compute, on the right hand side you will see filters
  - set system as ubuntu 22.04
  - then select a us based rtx gpu
  - click on configure
  - click on apps (select PyTorch JupyterLab <this runs on ubuntu 22.04 too>)
  - set disk size at least 40gb
  - click on deploy

> contributing to openmind
  - wait till status changes to "service configured"
  - click on it and select "access web ssh"
  - test if your server is up
    uptime

    if it shows time variables then it is up
  >/ install the basics (copy code below)

 apt-get update
apt-get install -y git curl build-essential python3-dev portaudio19-dev ffmpeg

     - right click on the web based terminal and select paste after copying the code above

  >/ install uv (python manager)

curl -LsSf https://astral.sh/uv/install.sh | sh
source $HOME/.cargo/env

     - right click and select paste then enter

  >/ now lets clone OM1 repo (copy the code)

git clone https://github.com/OpenMind/OM1.git
cd OM1
git submodule update --init
uv venv

    - right click, selct paste, enter

   >/ create your api key

    - visit: portal.openmind.org
    - signin with details you used for fabric website
    - create api key and copy it
    - remember to buy $2 api credits so the api can pull requests

   >/ set up your api key for the code
    - echo "OM_API_KEY=om1_live_YOUR_KEY_HERE" > .env
    - in the code above, replace the "om1_live_YOUR_KEY_HERE" with your newly created api key
      
      you should get
      echo "OM_API_KEY=yournewapikey" > .env

    - now copy it and paste in the command line, then enter
 
   > finally, lets run it (copy code below)
   
uv run src/run.py spot

    - right click, paste and enter
    - wait for it to download modules

    - after that, you should see outputs like
      INFO:root:Loading vision model...
      Object Detector INPUT
      AVAILABLE ACTIONS: move, speak, emotion

    - over here it is asking me to add api credits (stripe rekting me kek)

    >/ thats all for now, make sure you use the same account on the fabric platform on the api portal
       it takes time for the team to review and award the badge
       you can run it for a few (5) hours and then stop

goodluck
