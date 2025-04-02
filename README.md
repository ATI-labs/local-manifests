Installing Repos

        repo init -u https://github.com/ProjectEverest/manifest -b 14 --git-lfs

        git clone https://github.com/ATI-labs/local-manifests.git -b tmp .repo/local_manifests/
        
sync repo

        repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)

you should run this to fix boot problem on oplus sm8450 devices!!!

        bash <(curl -Ls https://raw.githubusercontent.com/ATI-labs/local-manifests/fix/fix.sh)

Signing builds:

        bash <(curl -Ls https://raw.githubusercontent.com/ATI-labs/local-manifests/sign/sign.sh)

for oneplus 10pro
        
        . build/envsetup.sh
        lunch lineage_wly-user
        mka everest -j$(nproc --all)

for realme gt2 pro
        
        . build/envsetup.sh
        lunch lineage_ferrarri-user
        mka everest -j$(nproc --all)
