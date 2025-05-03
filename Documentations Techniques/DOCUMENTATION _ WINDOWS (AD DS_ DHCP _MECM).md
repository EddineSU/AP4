---
title: 'DOCUMENTATION : WINDOWS (AD DS/ DHCP /MECM)'
tags: [DOC-AP4]

---

[toc]

# Installation de Windows Server Core/GUI

## Étapes d'Installation Initiales

1. **Sélection de la Clé d'Installation**
   ![setup key](https://hackmd.io/_uploads/BknfdT2tyx.png)
   *Remarque: Si vous souhaitez l'expérience bureau, sélectionnez cette option*

2. **Choix de la Version du Serveur**
   ![version (standard core)](https://hackmd.io/_uploads/rkoLup2Fke.png)
   *Standard Core sélectionné dans cet exemple*

3. **Acceptation des Conditions d'Utilisation**
   ![TOS agree](https://hackmd.io/_uploads/ryedua2tyx.png)
   *Cliquez sur "J'accepte les conditions de licence" et continuez*

4. **Sélection du Type d'Installation**
   ![Custom install](https://hackmd.io/_uploads/rJqddp3Y1e.png)
   *Choisissez "Personnalisé: Installer uniquement Windows (avancé)"*

5. **Sélection du Disque d'Installation**
   ![Install on main disk](https://hackmd.io/_uploads/BJZ9OphtJx.png)
   *Sélectionnez votre partition principale*

6. **Attente de la Fin de l'Installation**
   ![Wait for install](https://hackmd.io/_uploads/BJziOTnF1l.png)
   *La progression de l'installation sera affichée*

## Configuration du Mot de Passe Administrateur (Version GUI)

7. **Définition du Mot de Passe Administrateur**
   ![Set admin password](https://hackmd.io/_uploads/SJKvnOGqkl.png)
   *Entrez et confirmez un mot de passe fort pour le compte administrateur*

# Configuration Réseau

## Configuration de la Carte Réseau (Windows GUI)

1. **Accès au Panneau de Configuration**
   ![Open control panel](https://hackmd.io/_uploads/HJc4CMQq1l.png)
   *Ouvrez le Panneau de configuration depuis le menu Démarrer*

2. **Ouverture des Paramètres Réseau**
   ![Open Network and Sharing Center](https://hackmd.io/_uploads/rkY_Af7c1l.png)
   *Sélectionnez "Centre Réseau et partage"*

3. **Sélection de l'Interface Réseau**
   ![Select the network interface](https://hackmd.io/_uploads/H182RG7q1e.png)
   *Cliquez sur votre connexion réseau active*

4. **Accès aux Propriétés Réseau**
   ![Open properties](https://hackmd.io/_uploads/BkEyJQXqyx.png)
   *Cliquez sur le bouton "Propriétés"*

5. **Configuration des Paramètres IPv4**
   ![Modify IPV4](https://hackmd.io/_uploads/BkGiymX9ke.png)
   *Sélectionnez "Protocole Internet version 4 (TCP/IPv4)" et cliquez sur "Propriétés"*

6. **Saisie de la Configuration Réseau**
   ![Set settings then click OK](https://hackmd.io/_uploads/rJZRkmQ91x.png)
   *Entrez l'adresse IP, le masque de sous-réseau, la passerelle par défaut et les détails du serveur DNS*

## Renommage de l'Ordinateur (Windows GUI)

1. **Ouverture des Paramètres Système**
   ![Open Settings In PC name Section](https://hackmd.io/_uploads/SkkDzQQ9kl.png)
   *Accédez aux paramètres de nom du PC*

2. **Accès à l'Option de Renommage**
   ![Click Rename this PC](https://hackmd.io/_uploads/SJicfQmckg.png)
   *Cliquez sur le bouton "Renommer ce PC"*

3. **Saisie du Nouveau Nom d'Ordinateur**
   ![Add name then click next](https://hackmd.io/_uploads/HkpafQQc1g.png)
   *Tapez le nouveau nom et cliquez sur "Suivant"*

4. **Redémarrage du Serveur**
   ![Restart the server](https://hackmd.io/_uploads/S1ng77Qqkg.png)
   *Cliquez sur "Redémarrer maintenant" pour appliquer les changements*

## Configuration de la Carte Réseau (Windows Core)

1. **Accès à l'Utilitaire SConfig**
   ![Sconfig Main menu option 8 net config](https://hackmd.io/_uploads/rkKvmmdjkl.png)
   *Sélectionnez l'option 8 pour les paramètres réseau*

2. **Sélection de l'Adaptateur Réseau**
   ![Choose netcard index](https://hackmd.io/_uploads/HkZqXQuoJe.png)
   *Entrez le numéro d'index de votre adaptateur réseau*

3. **Configuration de l'Adresse IP**
   ![Set IP first (option 1)](https://hackmd.io/_uploads/HJi27mOokl.png)
   *Sélectionnez l'option 1 pour définir l'adresse IP*

4. **Choix de la Méthode d'Attribution IP**
   ![Static for a server](https://hackmd.io/_uploads/SyU7EQdo1g.png)
   *Sélectionnez "S" pour IP statique (recommandé pour les serveurs)*

5. **Saisie de l'Adresse IP**
   ![Set ip address](https://hackmd.io/_uploads/rJzUEQdikl.png)
   *Tapez l'adresse IP de votre serveur*

6. **Saisie du Masque de Sous-réseau**
   ![Set subnet mask](https://hackmd.io/_uploads/B13OVm_iyl.png)
   *Entrez le masque de sous-réseau (généralement 255.255.255.0)*

7. **Configuration de la Passerelle par Défaut**
   ![Set gateway](https://hackmd.io/_uploads/r15iE7dske.png)
   *Entrez l'adresse de la passerelle par défaut de votre réseau*

8. **Configuration des Paramètres DNS**
   ![Set DNS (option 2)](https://hackmd.io/_uploads/rkZxHQdoJx.png)
   *Sélectionnez l'option 2 pour définir les serveurs DNS*

9. **Configuration du DNS Primaire**
   ![Set dns server one (local)](https://hackmd.io/_uploads/HJTQBX_sJl.png)
   *Entrez l'adresse du serveur DNS primaire (souvent local)*

10. **Configuration du DNS Secondaire**
    ![Set dns server one (Second AD)](https://hackmd.io/_uploads/H1R8SQOoJl.png)
    *Entrez l'adresse du serveur DNS secondaire (souvent un autre serveur AD)*

## Renommage de l'Ordinateur (Windows Core)

1. **Accès aux Paramètres de Nom d'Ordinateur**
   ![Sconfig Main Menu option 2](https://hackmd.io/_uploads/H1P6X7m9kg.png)
   *Sélectionnez l'option 2 dans le menu principal SConfig*

2. **Saisie du Nouveau Nom d'Ordinateur**
   ![Name then press enter](https://hackmd.io/_uploads/B1KZ4Qmckg.png)
   *Tapez le nouveau nom du serveur et appuyez sur Entrée*

3. **Redémarrage du Serveur**
   ![Restart Server](https://hackmd.io/_uploads/BycmNm791e.png)
   *Redémarrez le serveur pour appliquer le changement de nom*

---

# Configuration des contrôleurs de domaine Active Directory sur Windows Core

## Aperçu général
Cette documentation vous guide à travers le processus de configuration de deux contrôleurs de domaine Active Directory à l'aide de Windows Server Core. La configuration est automatisée à l'aide de scripts PowerShell qui configurent tous les composants nécessaires.

## Prérequis
- Installations de Windows Server Core
- Accès administratif
- Connectivité réseau entre les serveurs

## Configuration du contrôleur de domaine principal

### Étape 1 : Quitter SConfig pour accéder à PowerShell
D'abord, quittez l'interface de configuration du serveur (SConfig) en sélectionnant l'option 15 pour accéder à la ligne de commande PowerShell.

![Exit Sconfig to go to powershell (option 15)](https://hackmd.io/_uploads/HJW-9X7cke.png)

### Étape 2 : Créer le script d'installation
1. Lancez le Bloc-notes pour créer un nouveau script PowerShell :
   ```powershell
   notepad AD-Install.PS1
   ```

![Ru: notepad AD-Install.PS1](https://hackmd.io/_uploads/H1uH5XX5Jg.png)

2. Une boîte de dialogue apparaîtra vous demandant si vous souhaitez créer un nouveau fichier. Cliquez sur **Oui**.

![Create File](https://hackmd.io/_uploads/SkhFcmX5Jg.png)

3. Collez le script d'installation AD dans le Bloc-notes et enregistrez le fichier.


```powershell!
#--------------------------------------------------------------------------
#- Created by:             David Rodriguez                                -
#- Blog:                   www.sysadmintutorials.com                      -
#- Modified by:            Maximilian Neu                                 -
#--------------------------------------------------------------------------
#-------------
#- Variables -                                         -
#-------------

# Network Variables
$ethipaddress = '172.16.10.20' # static IP Address of the server
$ethprefixlength = '24' # subnet mask - 24 = 255.255.255.0
$ethdefaultgw = '172.16.10.254' # default gateway
$ethdns = '127.0.0.1,172.16.10.21' # for multiple DNS you can append DNS entries with comma's
$globalsubnet = '172.16.10.0/24' # Global Subnet will be used in DNS Reverse Record and AD Sites and Services Subnet
$subnetlocation = 'Colmar'
$sitename = 'Colmar-Site' # Renames Default-First-Site within AD Sites and Services

# Active Directory Variables
$domainname = 'haut-rhin.gouv' # enter in your active directory domain

# Remote Desktop Variable
$enablerdp = 'yes' # to enable RDP, set this variable to yes. to disable RDP, set this variable to no

# Hostname Variables
$computername = 'VAD68COL01' # enter in your server name

# NTP Variables
$ntpserver1 = '0.fr.pool.ntp.org'
$ntpserver2 = '1.fr.pool.ntp.org'

# Timestamp
Function Timestamp {
    $Global:timestamp = Get-Date -Format "dd-MM-yyy_hh:mm:ss"
}

# Log File Location
$logfile = "C:\AD-Install\Windows-2022-AD-Deployment-log.txt"

# Create Log File
Write-Host "-= Get timestamp =-" -ForegroundColor Green

Timestamp

IF (Test-Path $logfile) {
    Write-Host "-= Logfile Exists =-" -ForegroundColor Yellow
}

ELSE {

    Write-Host "-= Creating Logfile =-" -ForegroundColor Green

    Try {
        New-Item -Path 'C:\AD-Install' -ItemType Directory | Out-Null
        New-Item -ItemType File -Path $logfile -ErrorAction Stop | Out-Null
        Write-Host "-= The file $($logfile) has been created =-" -ForegroundColor Green
    }
    Catch {
        Write-Warning -Message $("Could not create logfile. Error: " + $_.Exception.Message)
        Break;
    }
}

# Check Script Progress via Logfile

$firstcheck = Select-String -Path $logfile -Pattern "1-Basic-Server-Config-Complete"

IF (!$firstcheck) {

    # Add starting date and time
    Write-Host "-= 1-Basic-Server-Config-Complete, does not exist =-" -ForegroundColor Yellow

    Timestamp
    Add-Content $logfile "$($Timestamp) - Starting Active Directory Script"

    ## 1-Basic-Server-Config ##

    #------------
    #- Settings -
    #------------

    # Set Network
    Timestamp
    Try {
        # Get current IP configuration for the first enabled adapter
        $adapter = Get-NetAdapter | Where-Object { $_.Status -eq "Up" } | Select-Object -First 1
        $currentIP = Get-NetIPAddress -InterfaceIndex $adapter.ifIndex -AddressFamily IPv4

        Write-Host "-= Using network adapter: $($adapter.Name) =-" -ForegroundColor Yellow
        Add-Content $logfile "$($Timestamp) - Using network adapter: $($adapter.Name)"

        # Check if settings are already configured
        if ($currentIP.IPAddress -eq $ethipaddress -and 
            $currentIP.PrefixLength -eq $ethprefixlength) {
            Write-Host "-= Network settings already configured, skipping =-" -ForegroundColor Yellow
            Add-Content $logfile "$($Timestamp) - Network settings already configured, no changes needed"
        }
        else {
            New-NetIPAddress -IPAddress $ethipaddress -PrefixLength $ethprefixlength -DefaultGateway $ethdefaultgw -InterfaceIndex $adapter.ifIndex -ErrorAction Stop | Out-Null
            Set-DNSClientServerAddress -ServerAddresses $ethdns.Split(',') -InterfaceIndex $adapter.ifIndex -ErrorAction Stop
            Write-Host "-= IP Address successfully set to $($ethipaddress), subnet $($ethprefixlength), default gateway $($ethdefaultgw) and DNS Server $($ethdns) =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - IP Address successfully set to $($ethipaddress), subnet $($ethprefixlength), default gateway $($ethdefaultgw) and DNS Server $($ethdns)"
        }
    }
    Catch {
        Write-Warning -Message $("Failed to verify/apply network settings. Error: " + $_.Exception.Message)
        Break;
    }

    # Set RDP
    Timestamp
    Try {
        IF ($enablerdp -eq "yes") {
            Set-ItemProperty -Path 'HKLM:\System\CurrentControlSet\Control\Terminal Server'-name "fDenyTSConnections" -Value 0 -ErrorAction Stop
            Enable-NetFirewallRule -DisplayGroup "Remote Desktop" -ErrorAction Stop
            Write-Host "-= RDP Successfully enabled =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - RDP Successfully enabled"
        }
    }
    Catch {
        Write-Warning -Message $("Failed to enable RDP. Error: " + $_.Exception.Message)
        Break;
    }

    IF ($enablerdp -ne "yes") {
        Write-Host "-= RDP remains disabled =-" -ForegroundColor Green
        Add-Content $logfile "$($Timestamp) - RDP remains disabled"
    }

    # Set Hostname
    Timestamp
    Try {
        # Check if computer name already matches desired name
        if ($env:computername -eq $computername) {
            Write-Host "-= Computer name already set to $($computername), skipping rename =-" -ForegroundColor Yellow
            Add-Content $logfile "$($Timestamp) - Computer name already set to $($computername), no change needed"
        }
        else {
            Rename-Computer -ComputerName $env:computername -NewName $computername -ErrorAction Stop | Out-Null
            Write-Host "-= Computer name set to $($computername) =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Computer name set to $($computername)"
        }
    }
    Catch {
        Write-Warning -Message $("Failed to set new computer name. Error: " + $_.Exception.Message)
        Break;
    }

    # Add first script complete to logfile
    Timestamp
    Add-Content $logfile "$($Timestamp) - 1-Basic-Server-Config-Complete, starting script 2 =-"
        
    # Ask user before rebooting
    Timestamp
    $rebootChoice = Read-Host "The server needs to restart to apply changes. Do you want to restart now? (Y/N)"
        
    if ($rebootChoice -eq "Y" -or $rebootChoice -eq "y") {
        Write-Host "-= Save your work, computer will restart in 30 seconds =-" -ForegroundColor White -BackgroundColor Red
        Sleep 30

        Try {
            Restart-Computer -ComputerName $env:computername -ErrorAction Stop
            Write-Host "-= Rebooting now!! =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Rebooting now"
            Break;
        }
        Catch {
            Write-Warning -Message $("Failed to restart computer $($env:computername). Error: " + $_.Exception.Message)
            Break;
        }
    }
    else {
        Write-Warning "Restart postponed. Changes won't be applied until the server restarts."
        Add-Content $logfile "$($Timestamp) - Restart postponed by user"
    }

} # Close 'IF (!$firstcheck)'

# Check Script Progress via Logfile
$secondcheck1 = Get-Content $logfile | Where-Object { $_.Contains("1-Basic-Server-Config-Complete") }

IF ($secondcheck1) {
    $secondcheck2 = Get-Content $logfile | Where-Object { $_.Contains("2-Build-Active-Directory-Complete") }

    IF (!$secondcheck2) {

        ## 2-Build-Active-Directory ##

        Timestamp
        
        #-------------
        #- Variables -                                         -
        #-------------

        # Active Directory Variables
        $dsrmpassword = Read-Host "Enter Directory Services Restore Password" -AsSecureString

        #------------
        #- Settings -
        #------------

        # Install Active Directory Services
        Timestamp
        Try {
            Write-Host "-= Active Directory Domain Services installing =-" -ForegroundColor Yellow
            Install-WindowsFeature -name AD-Domain-Services -IncludeManagementTools
            Write-Host "-= Active Directory Domain Services installed successfully =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Active Directory Domain Services installed successfully"
        }
        Catch {
            Write-Warning -Message $("Failed to install Active Directory Domain Services. Error: " + $_.Exception.Message)
            Break;
        }

        # Configure Active Directory
        Timestamp
        Try {
            Write-Host "-= Configuring Active Directory Domain Services =-" -ForegroundColor Yellow
            Install-ADDSForest -DomainName $domainname -InstallDNS -ErrorAction Stop -NoRebootOnCompletion -SafeModeAdministratorPassword $dsrmpassword -Confirm:$false | Out-Null
            Write-Host "-= Active Directory Domain Services configured successfully =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Active Directory Domain Services configured successfully"
        }
        Catch {
            Write-Warning -Message $("Failed to configure Active Directory Domain Services. Error: " + $_.Exception.Message)
            Break;
        }

        # Add second script complete to logfile
        Timestamp
        Add-Content $logfile "$($Timestamp) - 2-Build-Active-Directory-Complete, starting script 3 =-"

        # Reboot Computer to apply settings
        Write-Host "-= Save all your work, computer rebooting in 30 seconds =-" -ForegroundColor White -BackgroundColor Red
        Sleep 30

        Try {
            Restart-Computer -ComputerName $env:computername -ErrorAction Stop
            Write-Host "Rebooting Now!!" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Rebooting Now!!"
            Break;
        }
        Catch {
            Write-Warning -Message $("Failed to restart computer $($env:computername). Error: " + $_.Exception.Message)
            Break;
        }
    } # Close 'IF ($secondcheck2)'
}# Close 'IF ($secondcheck1)'


# Add second script complete to logfile

# Check Script Progress via Logfile
$thirdcheck = Get-Content $logfile | Where-Object { $_.Contains("2-Build-Active-Directory-Complete") }

## 3-Build-Active-Directory ##

#------------
#- Settings -
#------------

# Add DNS Reverse Record
Timestamp
Try {
    Add-DnsServerPrimaryZone -NetworkId $globalsubnet -DynamicUpdate Secure -ReplicationScope Domain -ErrorAction Stop
    Write-Host "-= Successfully added in $($globalsubnet) as a reverse lookup within DNS =-" -ForegroundColor Green
    Add-Content $logfile "$($Timestamp) - Successfully added $($globalsubnet) as a reverse lookup within DNS"
}
Catch {
    Write-Warning -Message $("Failed to create reverse DNS lookups zone for network $($globalsubnet). Error: " + $_.Exception.Message)
    Break;
}

# Add DNS Scavenging
Write-Host "-= Set DNS Scavenging =-" -ForegroundColor Yellow

Timestamp
Try {
    Set-DnsServerScavenging -ScavengingState $true -ScavengingInterval 7.00:00:00 -Verbose -ErrorAction Stop
    Set-DnsServerZoneAging $domainname -Aging $true -RefreshInterval 7.00:00:00 -NoRefreshInterval 7.00:00:00 -Verbose -ErrorAction Stop
    Add-Content $logfile "$($Timestamp) - DNS Scavenging Complete"
}
Catch {
    Write-Warning -Message $("Failed to DNS Scavenging. Error: " + $_.Exception.Message)
    Break;
}

Get-DnsServerScavenging

Write-Host "-= DNS Scavenging Complete =-" -ForegroundColor Green

# Create Active Directory Sites and Services
Timestamp
Try {
    New-ADReplicationSubnet -Name $globalsubnet -Site "Default-First-Site-Name" -Location $subnetlocation -ErrorAction Stop
    Write-Host "-= Successfully added Subnet $($globalsubnet) with location $($subnetlocation) in AD Sites and Services =-" -ForegroundColor Green
    Add-Content $logfile "$($Timestamp) - Successfully added Subnet $($globalsubnet) with location $($subnetlocation) in AD Sites and Services"
}
Catch {
    Write-Warning -Message $("Failed to create Subnet $($globalsubnet) in AD Sites and Services. Error: " + $_.Exception.Message)
    Break;
}

# Rename Active Directory Site
Timestamp
Try {
    Get-ADReplicationSite Default-First-Site-Name | Rename-ADObject -NewName $sitename -ErrorAction Stop
    Write-Host "-= Successfully renamed Default-First-Site-Nameto $sitename in AD Sites and Services =-" -ForegroundColor Green
    Add-Content $logfile "$($Timestamp) - Successfully renamed Default-First-Site-Nameto $sitename in AD Sites and Services"
}
Catch {
    Write-Warning -Message $("Failed to rename site in AD Sites and Services. Error: " + $_.Exception.Message)
    Break;
}

# Add NTP settings to PDC

Timestamp

$serverpdc = Get-AdDomainController -Filter * | Where { $_.OperationMasterRoles -contains "PDCEmulator" }

IF ($serverpdc) {
    Try {
        Start-Process -FilePath "C:\Windows\System32\w32tm.exe" -ArgumentList "/config /manualpeerlist:$($ntpserver1),$($ntpserver2) /syncfromflags:MANUAL /reliable:yes /update" -ErrorAction Stop
        Stop-Service w32time -ErrorAction Stop
        sleep 2
        Start-Service w32time -ErrorAction Stop
        Write-Host "-= Successfully set NTP Servers: $($ntpserver1) and $($ntpserver2) =-" -ForegroundColor Green
        Add-Content $logfile "$($Timestamp) - Successfully set NTP Servers: $($ntpserver1) and $($ntpserver2)"
    }
    Catch {
        Write-Warning -Message $("Failed to set NTP Servers. Error: " + $_.Exception.Message)
        Break;
    }
}

# Script Finished

Timestamp
Write-Host "-= 3-Finalize-AD-Config Complete =-" -ForegroundColor Green
Add-Content $logfile "$($Timestamp) - 3-Finalize-AD-Config Complete"
Write-Host "-= Active Directory Script Complete =-" -ForegroundColor Green
Add-Content $logfile "$($Timestamp) - Active Directory Script Complete"
```

![Paste Script and save](https://hackmd.io/_uploads/SJhKsuOoJx.png)


### Étape 3 : Exécuter le script d'installation
Exécutez le script PowerShell pour installer et configurer Active Directory :

```powershell
.\AD-Install.ps1
```

![.\AD-Install.ps1](https://hackmd.io/_uploads/B1s7j7X5yl.png)

Le script effectuera plusieurs actions :
- Installation du rôle Services de domaine Active Directory
- Configuration du serveur en tant que contrôleur de domaine
- Configuration des services DNS
- Création de la structure de forêt et de domaine
- Configuration des paramètres nécessaires

![Run the script](https://hackmd.io/_uploads/S1OCyVQ51l.png)

## Configuration du contrôleur de domaine secondaire

### Étape 1 : Créer le script du DC secondaire
Créez un autre script PowerShell sur le second serveur en suivant le même processus, mais en utilisant le script pour le DC secondaire.
```powershell!
#--------------------------------------------------------------------------
#- Created by:             David Rodriguez                                -
#- Blog:                   www.sysadmintutorials.com                      -
#- Modified by:            Maximilian Neu                                 -
#- Modified for:           Secondary Domain Controller Setup              -
#--------------------------------------------------------------------------
#-------------
#- Variables -                                         -
#-------------

# Network Variables
$ethipaddress = '172.16.10.21' # static IP Address of the secondary DC
$ethprefixlength = '24' # subnet mask - 24 = 255.255.255.0
$ethdefaultgw = '172.16.10.254' # default gateway
$ethdns = '172.16.10.20,127.0.0.1' # Primary DC first, then localhost
$globalsubnet = '172.16.10.0/24' # Global Subnet will be used in DNS Reverse Record and AD Sites and Services Subnet
$subnetlocation = 'Colmar'
$sitename = 'Colmar-Site'

# Active Directory Variables
$domainname = 'haut-rhin.gouv' # enter in your active directory domain
$primaryDC = 'VAD68COL01' # name of the primary DC

# Remote Desktop Variable
$enablerdp = 'yes' # to enable RDP, set this variable to yes. to disable RDP, set this variable to no

# Hostname Variables
$computername = 'VAD68COL02' # secondary DC name

# Timestamp
Function Timestamp {
    $Global:timestamp = Get-Date -Format "dd-MM-yyy_hh:mm:ss"
}

# Log File Location
$logfile = "C:\AD-Install\Windows-2022-AD-Secondary-DC-Deployment-log.txt"

# Create Log File
Write-Host "-= Get timestamp =-" -ForegroundColor Green

Timestamp

IF (Test-Path $logfile) {
    Write-Host "-= Logfile Exists =-" -ForegroundColor Yellow
}
ELSE {
    Write-Host "-= Creating Logfile =-" -ForegroundColor Green

    Try {
        New-Item -Path 'C:\AD-Install' -ItemType Directory | Out-Null
        New-Item -ItemType File -Path $logfile -ErrorAction Stop | Out-Null
        Write-Host "-= The file $($logfile) has been created =-" -ForegroundColor Green
    }
    Catch {
        Write-Warning -Message $("Could not create logfile. Error: " + $_.Exception.Message)
        Break;
    }
}

# Check Script Progress via Logfile
$firstcheck = Select-String -Path $logfile -Pattern "1-Basic-Server-Config-Complete"

IF (!$firstcheck) {
    # Add starting date and time
    Write-Host "-= 1-Basic-Server-Config-Complete, does not exist =-" -ForegroundColor Yellow

    Timestamp
    Add-Content $logfile "$($Timestamp) - Starting Secondary DC Configuration Script"

    ## 1-Basic-Server-Config ##

    # Set Network
    Timestamp
    Try {
        $adapter = Get-NetAdapter | Where-Object { $_.Status -eq "Up" } | Select-Object -First 1
        $currentIP = Get-NetIPAddress -InterfaceIndex $adapter.ifIndex -AddressFamily IPv4

        Write-Host "-= Using network adapter: $($adapter.Name) =-" -ForegroundColor Yellow
        Add-Content $logfile "$($Timestamp) - Using network adapter: $($adapter.Name)"

        if ($currentIP.IPAddress -eq $ethipaddress -and 
            $currentIP.PrefixLength -eq $ethprefixlength) {
            Write-Host "-= Network settings already configured, skipping =-" -ForegroundColor Yellow
            Add-Content $logfile "$($Timestamp) - Network settings already configured, no changes needed"
        }
        else {
            New-NetIPAddress -IPAddress $ethipaddress -PrefixLength $ethprefixlength -DefaultGateway $ethdefaultgw -InterfaceIndex $adapter.ifIndex -ErrorAction Stop | Out-Null
            Set-DNSClientServerAddress -ServerAddresses $ethdns.Split(',') -InterfaceIndex $adapter.ifIndex -ErrorAction Stop
            Write-Host "-= IP Address successfully set to $($ethipaddress), subnet $($ethprefixlength), default gateway $($ethdefaultgw) and DNS Server $($ethdns) =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - IP Address successfully set"
        }
    }
    Catch {
        Write-Warning -Message $("Failed to verify/apply network settings. Error: " + $_.Exception.Message)
        Break;
    }

    # Set RDP
    Timestamp
    Try {
        IF ($enablerdp -eq "yes") {
            Set-ItemProperty -Path 'HKLM:\System\CurrentControlSet\Control\Terminal Server'-name "fDenyTSConnections" -Value 0 -ErrorAction Stop
            Enable-NetFirewallRule -DisplayGroup "Remote Desktop" -ErrorAction Stop
            Write-Host "-= RDP Successfully enabled =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - RDP Successfully enabled"
        }
    }
    Catch {
        Write-Warning -Message $("Failed to enable RDP. Error: " + $_.Exception.Message)
        Break;
    }

    # Set Hostname
    Timestamp
    Try {
        if ($env:computername -eq $computername) {
            Write-Host "-= Computer name already set to $($computername), skipping rename =-" -ForegroundColor Yellow
            Add-Content $logfile "$($Timestamp) - Computer name already set to $($computername), no change needed"
        }
        else {
            Rename-Computer -ComputerName $env:computername -NewName $computername -ErrorAction Stop | Out-Null
            Write-Host "-= Computer name set to $($computername) =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Computer name set to $($computername)"
        }
    }
    Catch {
        Write-Warning -Message $("Failed to set new computer name. Error: " + $_.Exception.Message)
        Break;
    }

    # Add first script complete to logfile
    Timestamp
    Add-Content $logfile "$($Timestamp) - 1-Basic-Server-Config-Complete"
        
    # Ask user before rebooting
    Timestamp
    $rebootChoice = Read-Host "The server needs to restart to apply changes. Do you want to restart now? (Y/N)"
        
    if ($rebootChoice -eq "Y" -or $rebootChoice -eq "y") {
        Write-Host "-= Save your work, computer will restart in 30 seconds =-" -ForegroundColor White -BackgroundColor Red
        Sleep 30

        Try {
            Restart-Computer -ComputerName $env:computername -ErrorAction Stop
            Write-Host "-= Rebooting now!! =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Rebooting now"
            Break;
        }
        Catch {
            Write-Warning -Message $("Failed to restart computer. Error: " + $_.Exception.Message)
            Break;
        }
    }
    else {
        Write-Warning "Restart postponed. Changes won't be applied until the server restarts."
        Add-Content $logfile "$($Timestamp) - Restart postponed by user"
    }
}

# Check Script Progress via Logfile
$secondcheck1 = Get-Content $logfile | Where-Object { $_.Contains("1-Basic-Server-Config-Complete") }

IF ($secondcheck1) {
    $secondcheck2 = Get-Content $logfile | Where-Object { $_.Contains("2-Join-Domain-Complete") }

    IF (!$secondcheck2) {
        ## 2-Join-Domain ##

        Timestamp
        
        # Install Active Directory Services
        Try {
            Write-Host "-= Active Directory Domain Services installing =-" -ForegroundColor Yellow
            Install-WindowsFeature -name AD-Domain-Services -IncludeManagementTools
            Write-Host "-= Active Directory Domain Services installed successfully =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Active Directory Domain Services installed successfully"
        }
        Catch {
            Write-Warning -Message $("Failed to install Active Directory Domain Services. Error: " + $_.Exception.Message)
            Break;
        }

        # Join Domain
        Timestamp
        Try {
            $domainCred = Get-Credential -Message "Enter Domain Admin credentials"
            
            Write-Host "-= Joining domain $($domainname) =-" -ForegroundColor Yellow
            Add-Computer -DomainName $domainname -Credential $domainCred -ErrorAction Stop
            
            Write-Host "-= Successfully joined domain $($domainname) =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Successfully joined domain $($domainname)"
        }
        Catch {
            Write-Warning -Message $("Failed to join domain. Error: " + $_.Exception.Message)
            Break;
        }

        # Promote to DC
        Timestamp
        Try {
            $domainCred = Get-Credential -Message "Enter Domain Admin credentials"
            $dsrmpassword = Read-Host "Enter Directory Services Restore Password" -AsSecureString
            
            Write-Host "-= Installing Active Directory Domain Services and promoting to Domain Controller =-" -ForegroundColor Yellow
            Install-ADDSDomainController -DomainName $domainname -InstallDNS -Credential $domainCred -SafeModeAdministratorPassword $dsrmpassword -NoRebootOnCompletion -NoGlobalCatalog:$false -CreateDnsDelegation:$false -CriticalReplicationOnly:$false

            Write-Host "-= Successfully promoted to Domain Controller =-" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Successfully promoted to Domain Controller"
        }
        Catch {
            Write-Warning -Message $("Failed to promote to Domain Controller. Error: " + $_.Exception.Message)
            Break;
        }

        # Add second script complete to logfile
        Timestamp
        Add-Content $logfile "$($Timestamp) - 2-Join-Domain-Complete"

        # Reboot Computer to apply settings
        Write-Host "-= Save all your work, computer rebooting in 30 seconds =-" -ForegroundColor White -BackgroundColor Red
        Sleep 30

        Try {
            Restart-Computer -ComputerName $env:computername -ErrorAction Stop
            Write-Host "Rebooting Now!!" -ForegroundColor Green
            Add-Content $logfile "$($Timestamp) - Rebooting Now!!"
            Break;
        }
        Catch {
            Write-Warning -Message $("Failed to restart computer. Error: " + $_.Exception.Message)
            Break;
        }
    }
}

# Script Finished
Timestamp
Write-Host "-= Active Directory Secondary DC Setup Complete =-" -ForegroundColor Green
Add-Content $logfile "$($Timestamp) - Active Directory Secondary DC Setup Complete"
```

### Étape 2 : Exécuter le script du DC secondaire
Exécutez le script sur le second serveur pour :
- Installer les Services de domaine Active Directory
- Joindre le domaine existant
- Promouvoir le serveur en contrôleur de domaine
- Configurer la réplication DNS

![Do the same for the second DC but with the above script](https://hackmd.io/_uploads/SkWjbVQqyx.png)

## Après l'installation
Une fois que les deux scripts sont terminés avec succès :
- Vérifiez la fonctionnalité du domaine
- Testez la réplication entre les contrôleurs de domaine
- Vérifiez les services DNS
- Configurez tous les rôles ou fonctionnalités supplémentaires

# Procédure pour rejoindre un PC Windows à un domaine

### Étape 1 : Accéder aux paramètres système
Ouvrez les paramètres Windows et naviguez vers la section "À propos" dans les paramètres système.

![Open Settings on About Your PC](https://hackmd.io/_uploads/BJVTI4Q5ke.png)

### Étape 2 : Accéder aux options avancées du système
Cliquez sur "Renommer ce PC (options avancées)" pour ouvrir les propriétés système.

![Rename this PC advanced](https://hackmd.io/_uploads/HJYMDVm5yx.png)

### Étape 3 : Modifier l'appartenance au domaine
Dans la fenêtre Propriétés système, cliquez sur le bouton "Modifier" pour changer l'appartenance au domaine.

![Change domain](https://hackmd.io/_uploads/ByPrvNQ5kl.png)

### Étape 4 : Spécifier le domaine
Dans la nouvelle fenêtre, sélectionnez l'option "Domaine" et entrez le nom du domaine auquel vous souhaitez joindre l'ordinateur, puis cliquez sur "OK".

![Enter Domain and click OK](https://hackmd.io/_uploads/rk1_vVXcke.png)

### Étape 5 : S'authentifier
Entrez les informations d'identification d'un compte ayant les droits de joindre des ordinateurs au domaine (généralement un compte administrateur de domaine).

![Authenticate](https://hackmd.io/_uploads/B1Yqv4Q9kl.png)

### Étape 6 : Finalisation
Une fois l'authentification réussie, vous verrez un message de bienvenue confirmant que l'ordinateur a bien été ajouté au domaine. Un redémarrage sera nécessaire pour appliquer les changements.

![Welcome to domain window](https://hackmd.io/_uploads/BkUeO4Xc1g.png)

# Gestion des serveurs Core depuis l'interface graphique

## Utilisation du Gestionnaire de serveur pour administrer des serveurs Windows Core

### Étape 1 : Lancer le Gestionnaire de serveur
Sur un serveur ou poste de travail Windows avec interface graphique, ouvrez le Gestionnaire de serveur depuis le menu Démarrer ou la barre des tâches.

![Open server manager](https://hackmd.io/_uploads/SJTmx779kl.png)

### Étape 2 : Ajouter des serveurs à gérer
Dans le Gestionnaire de serveur, faites un clic droit sur "Tous les serveurs" dans le panneau de gauche, puis sélectionnez "Ajouter des serveurs".

![Right click All Servers and click add Servers](https://hackmd.io/_uploads/HkVIeQX9kx.png)

### Étape 3 : Rechercher et ajouter les serveurs Core
Dans la fenêtre "Ajouter des serveurs" :
1. Utilisez l'onglet "Recherche Active Directory" pour trouver vos serveurs Core
2. Sélectionnez les serveurs Core que vous souhaitez gérer
3. Cliquez sur la flèche pour les déplacer vers la liste des serveurs sélectionnés
4. Cliquez sur "OK" pour ajouter ces serveurs à votre Gestionnaire de serveur

![Search/Add Servers](https://hackmd.io/_uploads/B1aIuE79Jg.png)

## Avantages de la gestion centralisée
- **Administration simplifiée** : Gestion de plusieurs serveurs Core depuis une seule interface
- **Efficacité opérationnelle** : Réduction du besoin de se connecter individuellement à chaque serveur
- **Surveillance unifiée** : Vue d'ensemble de l'état de tous les serveurs

## Fonctionnalités disponibles
- Installation et configuration de rôles et fonctionnalités
- Surveillance des performances et des événements
- Gestion des services
- Exécution de tâches administratives à distance

# Installation de DHCP sur les Serveurs Core via Interface Graphique

## Installation du rôle DHCP

### Étape 1 : Ouvrir le Gestionnaire de serveur
Lancez le Gestionnaire de serveur depuis un poste Windows avec interface graphique.

![Open server manager](https://hackmd.io/_uploads/SJTmx779kl.png)

### Étape 2 : Localiser les serveurs à configurer
Dans le Gestionnaire de serveur, identifiez les serveurs Core sur lesquels vous souhaitez installer le service DHCP.

![Find the server(s) you want to setup](https://hackmd.io/_uploads/BkWgo4Xiyl.png)

### Étape 3 : Ajouter des rôles
Faites un clic droit sur le premier serveur et sélectionnez **Ajouter des rôles et des fonctionnalités**.

![Right click and select Add Roles and Features (on the first of the servers)](https://hackmd.io/_uploads/HkkdsEmokl.png)

### Étape 4 : Sélectionner le type d'installation
Conservez l'option par défaut **Installation basée sur un rôle** et cliquez sur **Suivant**.

![Role based installation type (Click next and leave as default)](https://hackmd.io/_uploads/SkxjiE7jkx.png)

### Étape 5 : Sélectionner le serveur cible
Choisissez le serveur sur lequel vous souhaitez ajouter le rôle DHCP.

![Select the server to add the role to](https://hackmd.io/_uploads/S1T0j4mi1g.png)

### Étape 6 : Sélectionner le rôle DHCP
Cochez la case **Serveur DHCP** dans la liste des rôles disponibles.

![Tick DHCP](https://hackmd.io/_uploads/r1yG3N7j1l.png)

### Étape 7 : Fonctionnalités supplémentaires
Aucune fonctionnalité supplémentaire n'est nécessaire, cliquez sur **Suivant**.

![No need to add a feature so skip](https://hackmd.io/_uploads/Byzw2VXjkx.png)

### Étape 8 : Informations sur DHCP
Lisez les informations concernant le rôle DHCP et cliquez sur **Suivant**.

![Accept the DHCP explication](https://hackmd.io/_uploads/SJYY2VXiJl.png)

### Étape 9 : Confirmation et installation
Vérifiez les sélections et cliquez sur **Installer**.

![Confirm and install](https://hackmd.io/_uploads/B1js2Vmo1g.png)

### Étape 10 : Configuration post-installation
Une fois l'installation terminée, cliquez sur **Terminer la configuration du DHCP**.

![Click on complete DHCP config](https://hackmd.io/_uploads/HkiZaE7ikg.png)

### Étape 11 : Assistant de configuration DHCP
Cliquez sur **Suivant** après avoir lu la description.

![Click on next after reading description](https://hackmd.io/_uploads/SJiE6VXiyg.png)

### Étape 12 : Autorisation du serveur
Utilisez un compte d'administrateur de domaine pour autoriser les serveurs DHCP dans Active Directory.

![Use Domain Admin account to authorize servers into AD](https://hackmd.io/_uploads/rkXdTN7oyx.png)

### Étape 13 : Finalisation
Fermez l'assistant une fois la configuration terminée.

![Close when done](https://hackmd.io/_uploads/ByHTTE7sye.png)

Répétez ces étapes sur les autres serveurs que vous souhaitez configurer comme serveurs DHCP.

## Configuration du DHCP et de la haute disponibilité

### Étape 1 : Ouvrir le gestionnaire DHCP
Depuis le Gestionnaire de serveur, ouvrez le gestionnaire DHCP sur le serveur DHCP principal.

![From the server manager open the DHCP manager on the main DHCP server](https://hackmd.io/_uploads/Hy3dCEXiJl.png)

### Étape 2 : Ajouter les autres serveurs
Cliquez pour ajouter les autres serveurs DHCP au gestionnaire.

![Click on Add the other servers the manager](https://hackmd.io/_uploads/BymQyrmokg.png)

### Étape 3 : Sélection des serveurs
Ajoutez les autres serveurs DHCP à gérer.

![Add the other servers](https://hackmd.io/_uploads/BJItkBQiJl.png)

### Étape 4 : Création d'une étendue
Cliquez pour créer une nouvelle étendue DHCP.

![Click add create a scope](https://hackmd.io/_uploads/ByVUxSQjJx.png)

### Étape 5 : Assistant d'étendue
Cliquez sur **Suivant** pour démarrer l'assistant d'étendue.

![Next on scope wizard](https://hackmd.io/_uploads/HknmbSXiJl.png)

### Étape 6 : Nommer l'étendue
Donnez un nom à l'étendue puis cliquez sur **Suivant**.

![Give it a name then click next](https://hackmd.io/_uploads/rypt-Smsyx.png)

### Étape 7 : Configuration du sous-réseau
Définissez le sous-réseau et le masque pour l'étendue DHCP.

![Set subnet](https://hackmd.io/_uploads/SJlgMSQo1l.png)

### Étape 8 : Exclusions d'adresses
Aucune exclusion n'est nécessaire, cliquez sur **Suivant**.

![No need for exclusions](https://hackmd.io/_uploads/rk-ffB7jye.png)

### Étape 9 : Durée du bail
Configurez la durée du bail (2 jours est généralement approprié).

![Set lease length (2 days is generaly fine)](https://hackmd.io/_uploads/SJ54fSmoye.png)

### Étape 10 : Options DHCP
Configurez les options DHCP en cliquant sur **Suivant**.

![Config DHCP options](https://hackmd.io/_uploads/rkhvfHQskx.png)

### Étape 11 : Configuration de la passerelle
Ajoutez les adresses des routeurs pour le VLAN.

![Add VLAN router addresses](https://hackmd.io/_uploads/ryf3Gr7okg.png)

### Étape 12 : Configuration DNS
Conservez les contrôleurs de domaine comme serveurs DNS.

![Leave the DCs as DNS servers](https://hackmd.io/_uploads/ryAy7rXsJg.png)

### Étape 13 : WINS (ignorer)
N'activez pas WINS car il est obsolète et non sécurisé.

![Do not set WINS (unsafe/obsolete)](https://hackmd.io/_uploads/Bk1PmBQjkg.png)

### Étape 14 : Activation de l'étendue
Activez l'étendue que vous venez de créer.

![Activate scope](https://hackmd.io/_uploads/SJx5mBmsyg.png)

### Étape 15 : Finalisation de l'étendue
Terminez l'assistant d'étendue.

![Finish wizard](https://hackmd.io/_uploads/HJFi7Bmsyl.png)

### Étape 16 : Configuration du basculement
Faites un clic droit sur le serveur principal et sélectionnez **Configurer le basculement**.

![Right click main server and configure failover](https://hackmd.io/_uploads/SyKDESQsJe.png)

### Étape 17 : Sélection des étendues
Sélectionnez toutes les étendues pour le basculement.

![Select all scopes](https://hackmd.io/_uploads/rkV5VBmikg.png)

### Étape 18 : Serveur partenaire
Choisissez le serveur partenaire pour le basculement.

![Choose parter server](https://hackmd.io/_uploads/SysnNrXskx.png)

### Étape 19 : Confirmation du partenaire
Cliquez sur **Suivant** après avoir choisi le serveur partenaire.

![Click next after choosing](https://hackmd.io/_uploads/B1kySrQoye.png)

### Étape 20 : Configuration de la relation
Configurez les paramètres de la relation de basculement.

![Setup relationship](https://hackmd.io/_uploads/ry9mSBmoJg.png)

### Étape 21 : Finalisation du basculement
Terminez l'assistant de configuration du basculement.

![Finish wizard](https://hackmd.io/_uploads/ByxISHXo1g.png)

### Étape 22 : Confirmation
Fermez la fenêtre une fois la configuration réussie.

![Close when successful](https://hackmd.io/_uploads/SJnvSBXskl.png)


# Prérequis et Configuration pour l'installation de MECM

Ce document fournit un guide détaillé pour l'installation complète de Microsoft Endpoint Configuration Manager (MECM) avec captures d'écran.

## Installation de SQL Server 2019

Pour commencer l'installation de MECM, nous devons d'abord installer SQL Server qui servira de base de données pour notre environnement.

1. **Insertion du support d'installation**
   - Insérez le disque ISO de SQL Server dans le lecteur
   - Accédez au contenu du disque pour lancer l'installation

   ![Insérer le disque ISO de SQL SERVER](https://hackmd.io/_uploads/HJ4XiPQqyl.png)

2. **Lancement de l'installation**
   - Localisez et exécutez le fichier Setup.exe pour démarrer l'assistant d'installation
   - Attendez le chargement de l'assistant

   ![Exécuter Setup.exe](https://hackmd.io/_uploads/Sk-PsPXqJx.png)

3. **Sélection du type d'installation**
   - Sélectionnez l'option **"Nouvelle installation autonome de SQL Server ou ajout de fonctionnalités à une installation existante"**
   - Cette option permet d'installer une nouvelle instance complète

   ![Nouvelle installation autonome de SQL Server ou ajout de fonctionnalités à une installation existante](https://hackmd.io/_uploads/rkRIhPQ9ye.png)

4. **Saisie de la clé produit**
   - Entrez votre clé de produit SQL Server dans le champ prévu
   - La clé détermine l'édition de SQL Server qui sera installée

   ![Saisir la clé du produit](https://hackmd.io/_uploads/SJS16DX5ke.png)

5. **Acceptation des conditions de licence**
   - Lisez attentivement les termes du contrat de licence
   - Cochez la case pour accepter les conditions

   ![Accepter les conditions de licence](https://hackmd.io/_uploads/SkjW6v75kx.png)

6. **Configuration des mises à jour**
   - **Important** : Désactivez la vérification des mises à jour Microsoft
   - Cette configuration est recommandée pour éviter des problèmes pendant l'installation

   ![Ne pas activer la vérification des mises à jour](https://hackmd.io/_uploads/B1c86wQ9yx.png)

7. **Sélection des fonctionnalités**
   - Assurez-vous que **"Services de moteur de base de données"** est sélectionné
   - C'est le composant essentiel requis pour MECM

   ![Activer les services de moteur de base de données](https://hackmd.io/_uploads/HJGMCv7cJx.png)

8. **Configuration de l'instance**
   - Définissez un **ID d'instance** approprié
   - Vous pouvez utiliser l'instance par défaut (MSSQLSERVER) ou spécifier un nom personnalisé

   ![Définir l'ID d'instance](https://hackmd.io/_uploads/SkBT0wQ91g.png)

9. **Configuration des comptes de service**
   - **Action importante** : Créez deux comptes de service dédiés dans Active Directory
     * Un pour le service SQL Server Agent
     * Un pour le moteur de base de données SQL Server
   - Ces comptes séparés améliorent la sécurité et facilitent la maintenance

   ![Créer 2 comptes de service dans AD (Agent et Moteur)](https://hackmd.io/_uploads/SkGKxdmqyg.png)

10. **Ajout des comptes de service**
    - Entrez les informations des comptes de service créés
    - Spécifiez les mots de passe correspondants

    ![Ajouter les comptes de service](https://hackmd.io/_uploads/HkZ3nsX5kx.png)

11. **Vérification du classement**
    - Vérifiez que le classement est bien configuré pour votre région et vos besoins linguistiques
    - Le classement par défaut convient généralement pour la plupart des installations occidentales

    ![Vérifier le classement](https://hackmd.io/_uploads/Bk7STjQq1g.png)

12. **Configuration des administrateurs**
    - Ajoutez les comptes utilisateurs qui auront des droits d'administrateur sur la base de données
    - Cliquez ensuite sur l'onglet Mémoire pour continuer

    ![Ajouter les administrateurs et passer à la mémoire](https://hackmd.io/_uploads/rJ_vRjm5yx.png)

13. **Configuration de la mémoire**
    - Définissez la mémoire minimale pour SQL Server
    - Cette configuration est importante pour les performances optimales de la base de données

    ![Définir la mémoire minimale](https://hackmd.io/_uploads/B16IJ3Q9Jx.png)

14. **Confirmation et installation**
    - Vérifiez tous les paramètres dans le récapitulatif
    - Cliquez sur **Installer** pour démarrer l'installation

    ![Confirmer l'installation](https://hackmd.io/_uploads/rJrib3m5yg.png)

15. **Finalisation**
    - Une fois l'installation terminée, cliquez sur **Fermer**
    - L'installation de base de SQL Server est maintenant terminée

    ![Fermer](https://hackmd.io/_uploads/S1xsX27cyl.png)

### Configuration supplémentaire : Désactivation des ports TCP dynamiques

Pour garantir une connexion stable et cohérente entre MECM et SQL Server :

1. **Ouverture du gestionnaire de configuration**
   - Ouvrez le **Gestionnaire de configuration SQL Server 2019** depuis le menu Démarrer
   - Accédez à la section configuration du réseau

   ![Ouvrir le Gestionnaire de configuration SQL Server 2019](https://hackmd.io/_uploads/H14Qh1S51x.png)

2. **Configuration des ports**
   - **Action critique** : Assurez-vous qu'un port TCP statique est configuré
   - Désactivez les ports dynamiques pour améliorer la stabilité et la sécurité

   ![S'assurer qu'un port TCP statique est utilisé](https://hackmd.io/_uploads/H1feyxH91x.png)

### Installation de la mise à jour cumulative de SQL Server

Pour maintenir SQL Server à jour et corriger les problèmes connus :

1. **Lancement de l'installation de la mise à jour**
   - Exécutez le fichier d'installation de la dernière mise à jour cumulative
   - Attendez le chargement de l'assistant

   ![Lancer l'installation](https://hackmd.io/_uploads/SJtN15E91x.png)

2. **Vérification des prérequis**
   - L'assistant vérifie les conditions préalables
   - Cliquez sur **Suivant** pour continuer

   ![Page des prérequis, cliquer sur suivant](https://hackmd.io/_uploads/Hym7MiN5yl.png)

3. **Acceptation des conditions de licence**
   - Lisez et acceptez les termes du contrat de licence
   - Cochez la case correspondante

   ![Accepter les conditions de licence](https://hackmd.io/_uploads/Sk7UGiN5kl.png)

4. **Sélection des fonctionnalités**
   - Vérifiez que toutes les fonctionnalités installées sont sélectionnées
   - Cliquez sur **Suivant** pour continuer

   ![Sélectionner les fonctionnalités, cliquer sur suivant](https://hackmd.io/_uploads/ryrdfiVq1g.png)

5. **Gestion des fichiers en cours d'utilisation**
   - Si des fichiers sont en cours d'utilisation, l'assistant vous en informera
   - Cliquez sur **Suivant** pour continuer

   ![Fichier en cours d'utilisation, cliquer sur suivant](https://hackmd.io/_uploads/B1e4XoE9Jl.png)

6. **Lancement de la mise à jour**
   - Cliquez sur le bouton pour démarrer l'installation de la mise à jour
   - Attendez que le processus se termine

   ![Mettre à jour](https://hackmd.io/_uploads/B1SDXi4cJg.png)

7. **Finalisation**
   - Une fois la mise à jour terminée, cliquez sur **Terminer**
   - SQL Server est maintenant à jour

   ![Terminer](https://hackmd.io/_uploads/H1p9SsNqkl.png)

### Installation de SQL Server Management Studio (SSMS)

SSMS est l'outil d'administration principal pour SQL Server :

1. **Lancement de l'installation**
   - Exécutez le programme d'installation de SSMS
   - L'assistant d'installation se lance

   ![Exécuter SSMS](https://hackmd.io/_uploads/SyHz16X9yx.png)

2. **Installation**
   - Cliquez sur **Installer** pour démarrer l'installation de SSMS
   - Attendez que le processus d'installation se termine

   ![Installer SSMS](https://hackmd.io/_uploads/HyP0y67c1l.png)

3. **Finalisation**
   - Une fois l'installation terminée, cliquez sur **Fermer**
   - SSMS est maintenant disponible pour gérer SQL Server

   ![Fermer l'installation](https://hackmd.io/_uploads/BJuilaXqyl.png)

### Installation de Reporting Services

Reporting Services est nécessaire pour les rapports MECM :

1. **Lancement de l'installation**
   - Exécutez le programme d'installation de SQL Server Reporting Services
   - Attendez le chargement de l'assistant

   ![Lancer l'installation](https://hackmd.io/_uploads/ry52-pQ9Jg.png)

2. **Démarrage de l'installation**
   - Cliquez sur **Installer Reporting Services** pour commencer
   - Cette étape lance l'installation des composants principaux

   ![Installer Reporting Services](https://hackmd.io/_uploads/ByA7Ma7c1e.png)

3. **Sélection de l'édition**
   - **Important** : Choisissez l'édition qui correspond à votre édition de SQL Server
   - La correspondance des éditions est cruciale pour la compatibilité

   ![Choisir l'édition correspondant à SQL Server](https://hackmd.io/_uploads/ryB8T_Nckg.png)

4. **Acceptation des conditions**
   - Lisez et acceptez les conditions de licence
   - Cochez la case correspondante

   ![Accepter les conditions](https://hackmd.io/_uploads/ryRZQa7ckl.png)

5. **Installation du moteur**
   - L'assistant installe le moteur de base de données nécessaire
   - Attendez que cette étape se termine

   ![Installer le moteur de base de données](https://hackmd.io/_uploads/HkxB76Qc1e.png)

6. **Définition de l'emplacement**
   - Spécifiez l'emplacement d'installation souhaité
   - Vous pouvez conserver l'emplacement par défaut ou le personnaliser

   ![Emplacement d'installation](https://hackmd.io/_uploads/BJVK7p791l.png)

7. **Configuration du serveur de rapports**
   - Lancez l'outil de configuration du serveur de rapports
   - Cette étape est nécessaire pour finaliser l'installation

   ![Configurer le serveur de rapports](https://hackmd.io/_uploads/BJH7V6Q5Jg.png)

8. **Connexion au serveur de rapports**
   - Établissez la connexion au serveur de rapports
   - Vérifiez que la connexion fonctionne correctement

   ![Se connecter au serveur de rapports](https://hackmd.io/_uploads/HJEcE6Q5kg.png)

### Installation du pilote ODBC pour SQL

Le pilote ODBC permet aux applications de communiquer avec SQL Server :

1. **Lancement de l'installation**
   - Exécutez le programme d'installation du pilote ODBC
   - L'assistant d'installation se lance

   ![Lancer l'installation](https://hackmd.io/_uploads/ByUhn8Ncye.png)

2. **Écran d'accueil**
   - Cliquez sur **Suivant** sur l'écran de bienvenue
   - Cela vous mène aux étapes suivantes de l'installation

   ![Suivant sur l'écran d'accueil de l'assistant](https://hackmd.io/_uploads/S1MJTLE9Je.png)

3. **Acceptation des conditions de licence**
   - Lisez et acceptez les conditions de licence
   - Cochez la case puis cliquez sur **Suivant**

   ![Accepter les conditions de licence](https://hackmd.io/_uploads/r1dbTLN5kl.png)

4. **Sélection des fonctionnalités**
   - **Important** : Sélectionnez les deux fonctionnalités proposées
   - Les deux composants sont nécessaires pour une compatibilité complète

   ![Sélectionner les deux fonctionnalités](https://hackmd.io/_uploads/Sy1SaUVcJg.png)

5. **Finalisation**
   - Une fois l'installation terminée, cliquez sur **Terminer**
   - Le pilote ODBC est maintenant installé et prêt à être utilisé

   ![Terminer l'installation](https://hackmd.io/_uploads/SkFwpL451l.png)


### Installation de Windows ADK

Windows ADK (Assessment and Deployment Kit) est nécessaire pour les fonctionnalités de déploiement de MECM :

1. **Lancement de l'installation**
   - Exécutez le fichier adkSetup.exe pour démarrer l'installation
   - Attendez le chargement de l'assistant

   ![Lancer adkSetup](https://hackmd.io/_uploads/H1louLE9Jl.png)

2. **Définition de l'emplacement**
   - Spécifiez l'emplacement d'installation souhaité
   - Vous pouvez conserver l'emplacement par défaut ou le personnaliser

   ![Définir l'emplacement d'installation](https://hackmd.io/_uploads/S1zGKUNqye.png)

3. **Configuration de la télémétrie**
   - **Recommandé** : Désactivez la télémétrie pour des raisons de confidentialité
   - Sélectionnez l'option correspondante

   ![Désactiver la télémétrie](https://hackmd.io/_uploads/SkbStLE9kl.png)

4. **Acceptation de la licence**
   - Lisez et acceptez les conditions de licence
   - Cochez la case correspondante

   ![Accepter la licence](https://hackmd.io/_uploads/S18vYLN5kx.png)

5. **Sélection des composants**
   - Sélectionnez les outils suivants :
     * Outils de déploiement
     * ICD (Imaging and Configuration Designer)
     * Concepteur de configuration
     * USMT (User State Migration Tool)

   ![Installer les outils de déploiement, ICD, concepteur de configuration, USMT](https://hackmd.io/_uploads/HkVJiLN5kl.png)

### Installation du complément WinPE

WinPE (Windows Preinstallation Environment) est nécessaire pour les fonctionnalités de déploiement avancées :

1. **Lancement de l'installation**
   - Exécutez le fichier adkwinpesetup.exe
   - Attendez le chargement de l'assistant

   ![Lancer adkwinpesetup](https://hackmd.io/_uploads/HkhKcOE9yl.png)

2. **Définition de l'emplacement**
   - Utilisez l'emplacement d'installation par défaut
   - Cliquez sur **Suivant** pour continuer

   ![Emplacement d'installation par défaut](https://hackmd.io/_uploads/rkKn9ONqyg.png)

3. **Configuration de la télémétrie**
   - Désactivez la collecte de données de télémétrie
   - Sélectionnez l'option correspondante

   ![Télémétrie désactivée](https://hackmd.io/_uploads/SyT09dNckg.png)

4. **Acceptation des conditions**
   - Lisez et acceptez les conditions de licence
   - Cochez la case puis cliquez sur **Suivant**

   ![Accepter les conditions](https://hackmd.io/_uploads/SJOejdN91e.png)

5. **Confirmation des fonctionnalités**
   - Vérifiez que les bonnes fonctionnalités sont sélectionnées
   - Cliquez sur **Installer** pour continuer

   ![Confirmer les fonctionnalités](https://hackmd.io/_uploads/H1QGj_45yx.png)

6. **Finalisation**
   - Une fois l'installation terminée, cliquez sur **Fermer**
   - Le complément WinPE est maintenant installé

   ![Fermer après l'installation](https://hackmd.io/_uploads/HkkOUKN51x.png)

### Extension du schéma AD

Pour que MECM fonctionne correctement avec Active Directory, le schéma doit être étendu :

1. **Configuration des permissions**
   - **Action critique** : Ajoutez les administrateurs au groupe "Schema Admins"
   - Cette appartenance est nécessaire pour modifier le schéma AD

   ![Ajouter les administrateurs au groupe d'administrateurs du schéma](https://hackmd.io/_uploads/Skdn_DNckx.png)

2. **Exécution de l'extension de schéma**
   - Accédez au dossier `(Support d'installation):\SMSSETUP\BIN\X64`
   - **Important** : Exécutez la commande `.\extadsch.exe` dans l'invite de commande

   ![Exécuter . \extadsch.exe dans cmd](https://hackmd.io/_uploads/rkffOvE51e.png)

3. **Vérification de l'installation**
   - Assurez-vous que l'extension a été appliquée avec succès
   - Recherchez le message de confirmation

   ![Installation réussie](https://hackmd.io/_uploads/HJietv49Jg.png)

### Création du conteneur System Management

Un conteneur spécial dans AD est nécessaire pour MECM :

1. **Ouverture de l'éditeur ADSO**
   - Ouvrez l'éditeur ADSO pour modifier la structure d'Active Directory
   - Cet outil permet de créer des objets dans AD

   ![Ouvrir ADSO edit](https://hackmd.io/_uploads/H1EQsD491g.png)

2. **Connexion à AD**
   - Établissez la connexion à votre serveur Active Directory
   - Entrez les informations d'identification si nécessaire

   ![Se connecter à AD](https://hackmd.io/_uploads/HkgwowNckg.png)

3. **Configuration du contexte de nommage**
   - Définissez le contexte de nommage par défaut pour votre domaine
   - Cette étape est cruciale pour naviguer dans la structure AD

   ![Définir le contexte de nommage par défaut](https://hackmd.io/_uploads/H1_OiP45Jg.png)

4. **Ajout d'un objet dans System**
   - Naviguez jusqu'à CN=System dans votre domaine
   - Préparez-vous à ajouter un nouvel objet conteneur

   ![Ajouter un objet à CN=System](https://hackmd.io/_uploads/B1EypwV9kx.png)

5. **Création du conteneur**
   - Créez un nouveau conteneur dans le dossier System
   - Cette étape prépare le conteneur principal

   ![Créer un conteneur](https://hackmd.io/_uploads/HJrM6DE91g.png)

6. **Nommage du conteneur**
   - **Important** : Nommez le conteneur "System Management"
   - Le nom exact est crucial pour la compatibilité avec MECM

   ![Créer System Management](https://hackmd.io/_uploads/H1VZADE9Je.png)

7. **Finalisation**
   - Cliquez sur **Terminer** pour créer le conteneur
   - Le conteneur System Management est maintenant créé

   ![Cliquer sur Terminer](https://hackmd.io/_uploads/BJPECDEckl.png)

### Configuration des autorisations du conteneur

Pour que le serveur MECM puisse accéder au conteneur System Management :

1. **Accès aux propriétés**
   - Ouvrez les propriétés du conteneur System Management
   - Utilisez l'outil Utilisateurs et ordinateurs Active Directory

    ![Ouvrir les propriétés de System Management](https://hackmd.io/_uploads/BkEdIYuo1x.png)

2. **Ajout de l'ordinateur**
   - Ajoutez l'ordinateur qui hébergera MECM aux propriétés de sécurité
   - Cliquez sur le bouton Ajouter

   ![Ajouter l'ordinateur aux propriétés de sécurité](https://hackmd.io/_uploads/HkuvkuN91l.png)

3. **Configuration des permissions**
   - **Crucial** : Accordez le contrôle total à l'ordinateur MECM
   - Appliquez les modifications pour enregistrer les autorisations

   ![Donner le contrôle total, puis appliquer](https://hackmd.io/_uploads/B1xae_4qJg.png)

### Installation des rôles et fonctionnalités Windows Server

Plusieurs rôles et fonctionnalités Windows Server sont requis pour MECM :

1. **Ouverture du gestionnaire de serveur**
   - Lancez le Gestionnaire de serveur
   - Cliquez sur **Ajouter des rôles et des fonctionnalités**

   ![Gestionnaire de serveur Ajouter des rôles/fonctionnalités](https://hackmd.io/_uploads/rkC04wX5Jl.png)

2. **Sélection du type d'installation**
   - Choisissez l'installation basée sur un rôle ou une fonctionnalité
   - Cliquez sur **Suivant** pour continuer

   ![Type d'installation](https://hackmd.io/_uploads/HyybrPm5kx.png)

3. **Sélection du serveur**
   - Sélectionnez le serveur qui hébergera MECM
   - Généralement, il s'agit du serveur local

   ![Sélectionner le serveur MECM](https://hackmd.io/_uploads/BJofHvXqkl.png)

4. **Sélection des rôles**
   - Ajoutez les rôles suivants :
     * **IIS** (Internet Information Services)
     * **WDS** (Windows Deployment Services)
     * **WSUS** (Windows Server Update Services)

   ![Ajouter les rôles (IIS) et WDS et WSUS](https://hackmd.io/_uploads/H1Qj7uNqkl.png)

5. **Sélection des fonctionnalités**
   - Ajoutez les fonctionnalités suivantes :
     * **.NET Framework 3.5**
     * **BITS** (Background Intelligent Transfer Service)
     * **Compression différentielle distante**

   ![Ajouter des fonctionnalités (.NET 3.5, BITS, compression différentielle distante)](https://hackmd.io/_uploads/HJAYEdEq1e.png)

6. **Configuration de WDS**
   - Dans la section WDS générale, cliquez sur **Suivant**
   - Cette étape utilise les paramètres par défaut

   ![WDS général: SUIVANT](https://hackmd.io/_uploads/HJSCE_V91e.png)

7. **Configuration des rôles WDS**
   - Acceptez les rôles par défaut pour WDS
   - Cliquez sur **Suivant** pour continuer

   ![Rôles WDS: SUIVANT](https://hackmd.io/_uploads/SygxB_45Jg.png)

8. **Configuration de WSUS**
   - Dans la section WSUS générale, cliquez sur **Suivant**
   - Cette étape utilise les paramètres par défaut

   ![WSUS général: SUIVANT](https://hackmd.io/_uploads/By3zru4q1g.png)

9. **Configuration des rôles WSUS**
   - **Important** : Ajoutez SQL comme base de données pour WSUS
   - Cliquez sur **Suivant** pour continuer

   ![Rôles WSUS: ajouter SQL puis SUIVANT](https://hackmd.io/_uploads/BkWuB_N9Jg.png)

10. **Définition de l'emplacement WSUS**
    - Acceptez l'emplacement par défaut ou spécifiez un nouvel emplacement
    - Cliquez sur **Suivant** pour continuer

    ![Emplacement WSUS: SUIVANT](https://hackmd.io/_uploads/r15aSdE51x.png)

11. **Connexion à la base de données**
    - Configurez la connexion à la base de données SQL Server
    - Entrez les informations de connexion requises

    ![WSUS: Se connecter à la base de données](https://hackmd.io/_uploads/H1NVI_Vqyx.png)

12. **Confirmation**
    - Vérifiez le récapitulatif des sélections
    - Cliquez sur **Installer** pour démarrer l'installation

    ![Confirmer](https://hackmd.io/_uploads/r1ePLOVc1g.png)

13. **Finalisation**
    - Une fois l'installation terminée, cliquez sur **Terminer**
    - Les rôles et fonctionnalités nécessaires sont maintenant installés

    ![Terminer](https://hackmd.io/_uploads/Byf5DOEqyx.png)

# Installation du site autonome principal MECM

Maintenant que tous les prérequis sont en place, nous pouvons installer MECM :

1. **Préparation du support**
   - Insérez le disque ISO MECM dans le lecteur
   - Accédez au contenu du disque
   ![Insérer le disque ISO MECM](https://hackmd.io/_uploads/BJ2OzPmc1e.png)

2. **Lancement de l'installation**
   - Exécutez l'utilitaire Splash.hta pour démarrer l'installation
   - Attendez le chargement de l'assistant
   ![Exécuter l'utilitaire Splash](https://hackmd.io/_uploads/HyFTGPmcJl.png)

3. **Démarrage de l'installation**
   - Cliquez sur le bouton **Installer** pour commencer
   - Cette étape lance l'assistant d'installation principal
   ![Cliquer sur Installer](https://hackmd.io/_uploads/H1wemwXq1x.png)

4. **Vérification des prérequis**
   - L'assistant vérifie que tous les prérequis sont installés
   - Acceptez la vérification pour continuer
   ![Accepter les prérequis](https://hackmd.io/_uploads/HJx9sUV9Jg.png)

5. **Sélection du type de site**
   - Sélectionnez **Site principal** comme type de site
   - Cette option crée un nouveau site MECM autonome
   ![Sélectionner le site principal](https://hackmd.io/_uploads/BJ2J4YV9kl.png)

6. **Saisie de la clé produit**
   - Entrez votre clé de produit MECM
   - La clé détermine la licence et les fonctionnalités disponibles
   ![Ajouter la clé du produit](https://hackmd.io/_uploads/BkTy1vNqyl.png)

7. **Acceptation de la licence**
   - Lisez et acceptez les conditions de licence
   - Cochez la case correspondante
   ![Accepter la licence](https://hackmd.io/_uploads/HkQ7kDEc1g.png)

8. **Configuration du dépôt de téléchargement**
   - Spécifiez l'emplacement où les fichiers téléchargés seront stockés
   - Assurez-vous qu'il y a suffisamment d'espace disque
   ![Définir le dépôt de téléchargement](https://hackmd.io/_uploads/SJRvyw45Jl.png)

9. **Sélection des langues du serveur**
   - Ajoutez les langues qui seront prises en charge par le serveur MECM
   - Sélectionnez au moins votre langue principale
   ![Ajouter les langues du serveur](https://hackmd.io/_uploads/Sk-_Nt4c1g.png)

10. **Sélection des langues du client**
    - Ajoutez les langues qui seront prises en charge par les clients MECM
    - Sélectionnez toutes les langues nécessaires pour votre environnement
    ![Ajouter les langues du client](https://hackmd.io/_uploads/HkmerYNcyg.png)

11. **Configuration du site**
    - **Important** : Définissez le code et le nom du site
    - Le code de site doit être unique (3 caractères alphanumériques)
    - Le nom du site doit être descriptif
    ![Définir le code et le nom du site](https://hackmd.io/_uploads/BkP1rwVcyl.png)

12. **Type d'installation**
    - Sélectionnez l'installation comme **site autonome**
    - Cette option crée un nouveau site principal indépendant
    ![Installer comme site autonome](https://hackmd.io/_uploads/SJJBSFN5Je.png)

13. **Confirmation du mode d'installation**
    - Un message s'affiche pour confirmer l'installation en tant que site autonome
    - Cliquez sur **Oui** pour continuer
    ![Popup: cliquer sur oui](https://hackmd.io/_uploads/HJEwRLN51x.png)

14. **Configuration de la base de données**
    - Renseignez les informations de configuration pour la base de données SQL
    - Assurez-vous que les paramètres correspondent à votre environnement
    ![Configuration des informations de la base de données](https://hackmd.io/_uploads/SyI5BKNq1x.png)

15. **Chemin d'accès à la base de données SQL**
    - Spécifiez l'emplacement des fichiers de la base de données SQL
    - Vérifiez que l'espace disque est suffisant à l'emplacement indiqué
    ![Chemin d'accès à la base de données SQL](https://hackmd.io/_uploads/Syz2C3E9Jg.png)

16. **Configuration du fournisseur SMS**
    - Configurez le fournisseur SMS qui gère les interactions avec la base de données
    - Généralement, vous pouvez conserver les paramètres par défaut
    ![Configuration du fournisseur SMS](https://hackmd.io/_uploads/HyK0AhV5yx.png)

17. **Configuration HTTP/HTTPS**
    - Définissez les paramètres de communication HTTP/HTTPS
    - Ces paramètres sont essentiels pour la sécurité des communications
    ![Configuration HTTP/HTTPS](https://hackmd.io/_uploads/H1gXy6V9kg.png)

18. **Installation des rôles de serveur**
    - Sélectionnez d'installer le point de gestion et le point de distribution
    - Ces rôles sont nécessaires pour la gestion des clients
    ![Installation du point de gestion et du point de distribution](https://hackmd.io/_uploads/HkU8yTEcyx.png)

19. **Collecte de données**
    - Acceptez ou refusez la collecte de données pour Microsoft
    - Cette étape est facultative mais aide à améliorer le produit
    ![Accepter la collecte de données](https://hackmd.io/_uploads/BJlmrPEqkg.png)

20. **Point de connexion de service**
    - Configurez le point de connexion de service
    - Ce composant permet la communication avec les services cloud
    ![Autoriser le point de connexion](https://hackmd.io/_uploads/SyA8BvN5ye.png)

21. **Résumé de l'installation**
    - Vérifiez le résumé des paramètres d'installation
    - Assurez-vous que tous les paramètres sont corrects avant de continuer
    ![Accepter le résumé](https://hackmd.io/_uploads/SJ0316N51g.png)

22. **Vérification finale des prérequis**
    - L'assistant effectue une dernière vérification des prérequis
    - Cliquez sur **Commencer l'installation** pour lancer le processus
    ![Commencer l'installation après vérification des prérequis](https://hackmd.io/_uploads/B1nh1lHqJe.png)

23. **Finalisation de l'installation**
    - Une fois l'installation terminée, vous verrez l'écran de confirmation
    - Cliquez sur **Fermer** pour terminer l'assistant
    ![Fermer après la fin de l'installation](https://hackmd.io/_uploads/S1fXkZr9Jx.png)

Félicitations ! Vous avez maintenant installé avec succès un site principal autonome MECM. Vous pouvez commencer à configurer votre environnement et à déployer des clients sur votre réseau.
# MECM : Configuration de la découverte Active Directory (AD)

---

### 1. **Accéder à la console Configuration Manager**

![Ouverture de Configuration Manager](https://hackmd.io/_uploads/B1dSPyP2Jl.png)

---

### 2. **Naviguer vers l’administration**

- Sélectionner `Administration`

![Accès à l'administration](https://hackmd.io/_uploads/SyGtD1vhke.png)

- Cliquer sur **Discovery Methods**

![Méthodes de découverte](https://hackmd.io/_uploads/rkx0PJvnkl.png)

---

### 3. **Découverte de la forêt Active Directory**

- Clic droit sur `Active Directory Forest Discovery` → **Properties**

![Propriétés Forest Discovery](https://hackmd.io/_uploads/HJ2xtJPhkx.png)

- Cocher **Enable Active Directory Forest Discovery**

![Activer Forest Discovery](https://hackmd.io/_uploads/SyiFtkvhkl.png)

---

### 4. **Découverte des groupes AD**

- Clic droit sur `Active Directory Group Discovery` → **Properties**

![Ajouter un groupe](https://hackmd.io/_uploads/Byc4qyPnJl.png)

- Nommer et sélectionner un groupe AD cible

![Sélection d’un groupe](https://hackmd.io/_uploads/rkr95Jvhkg.png)

- Appliquer et activer la découverte

![Activer la découverte de groupes](https://hackmd.io/_uploads/ry86ckw3yg.png)

---

### 5. **Découverte des systèmes AD**

- Clic droit sur `Active Directory System Discovery` → **Properties**

![Ajouter une unité d’organisation (OU)](https://hackmd.io/_uploads/H12Fs1Pnke.png)

- Appliquer

![Appliquer la config](https://hackmd.io/_uploads/SJ8z21whkg.png)

- Activer la découverte

![Activer découverte des systèmes](https://hackmd.io/_uploads/ByG-6kvn1x.png)

---

### 6. **Découverte des utilisateurs AD**

- Clic droit sur `Active Directory User Discovery` → **Properties**

![Ajouter un groupe utilisateur](https://hackmd.io/_uploads/BySpayP2kx.png)

- Appliquer

![Appliquer découverte utilisateur](https://hackmd.io/_uploads/BywbC1v2yg.png)

---

## MECM : Configuration du point de mise à jour logicielle & reporting

### 1. **Accéder à la configuration du site**

- Naviguer vers `Site Configuration > Sites`

![Accès à la configuration du site](https://hackmd.io/_uploads/rJl9sev2yl.png)

- Clic droit > **Add Site System Roles**

![Ajouter un rôle système](https://hackmd.io/_uploads/HkTh3eP3Jl.png)

---

### 2. **Configuration des rôles**

- **Général** : Suivant

![Général](https://hackmd.io/_uploads/By3e6xD3Jg.png)

- **Proxy** : Suivant

![Proxy](https://hackmd.io/_uploads/SJhMplP31g.png)

- Sélectionner :
  - **Software Update Point**
  - **Reporting Services Point**

![Sélection des rôles](https://hackmd.io/_uploads/HyV8agDnkx.png)

---

### 3. **Paramètres WSUS et synchronisation**

- Spécifier les ports et autoriser les connexions

![Ports et autorisation](https://hackmd.io/_uploads/Skpee-D31g.png)

- Ignorer proxy et compte

![Ignorer compte proxy](https://hackmd.io/_uploads/Hyawg-D3yl.png)

- Activer la synchro Microsoft & logs

![Activer sync et status logs](https://hackmd.io/_uploads/SySRlWwhkg.png)

- Planifier la synchro (ex : toutes les 2 semaines)

![Planification synchro](https://hackmd.io/_uploads/B1z8bWvnyl.png)

---

### 4. **Affinage des mises à jour**

- Ignorer les mises à jour remplacées

![Ignorer superseeded updates](https://hackmd.io/_uploads/HyVoZWvhkg.png)

- Supprimer les MAJ non utilisées

![Supprimer MAJ non utilisées](https://hackmd.io/_uploads/Sk8MfZv3kl.png)

- Configurer la durée max de déploiement

![Temps max de mise à jour](https://hackmd.io/_uploads/SkBG7-wn1x.png)

- Choisir uniquement les MAJ complètes

![MAJ complètes uniquement](https://hackmd.io/_uploads/S1YPm-D3kl.png)

- Sélectionner les catégories, produits, langues :

  - **Catégories :**
    ![Catégories MAJ](https://hackmd.io/_uploads/rkx6XWDhJe.png)

  - **Produits :**
    ![Produits à mettre à jour](https://hackmd.io/_uploads/BkDSEZw3yx.png)

  - **Langues :**
    ![Langues](https://hackmd.io/_uploads/BkjqEWDhJg.png)

---

## MECM : Création de média de séquence de tâches

### 1. **Créer un média de séquence de tâches**

![Créer média task sequence](https://hackmd.io/_uploads/S1FV8wzCyx.png)

- Choisir **Capture Media**

![Capture media](https://hackmd.io/_uploads/S1VdLPMCkg.png)

- Définir le type de média et l'emplacement :

![Type et emplacement média](https://hackmd.io/_uploads/HycpUPGC1g.png)
