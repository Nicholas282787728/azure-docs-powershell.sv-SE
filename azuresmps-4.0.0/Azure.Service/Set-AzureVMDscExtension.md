---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100581"
---
# <span data-ttu-id="dcb48-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dcb48-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="dcb48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcb48-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb48-103">Konfigurerar DSC-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dcb48-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="dcb48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcb48-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcb48-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcb48-105">DESCRIPTION</span></span>
<span data-ttu-id="dcb48-106">Cmdleten **set-AzureVMDscExtension** konfigurerar fil tillägget för önskad tillstånds konfiguration (DSC) på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dcb48-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="dcb48-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcb48-107">EXAMPLES</span></span>

### <span data-ttu-id="dcb48-108">Exempel 1: Konfigurera DSC-tillägget på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="dcb48-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="dcb48-109">Det här kommandot konfigurerar DSC-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dcb48-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="dcb48-110">Det MyConfiguration.ps1.zip paketet måste ha laddats upp tidigare till Azure Storage med kommandot **publicering-AzureVMDscConfiguration** och inkluderar MyConfiguration.ps1-skript och moduler det är beroende av.</span><span class="sxs-lookup"><span data-stu-id="dcb48-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="dcb48-111">Argumentet för konfiguration visar vilken DSC-konfiguration du kan använda för att köra det.</span><span class="sxs-lookup"><span data-stu-id="dcb48-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="dcb48-112">Parametern- *ConfigurationArgument* anger en hash med de argument som skickas till funktionen konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dcb48-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="dcb48-113">Exempel 2: Konfigurera DSC-tillägget på en virtuell dator med en sökväg till konfigurations data</span><span class="sxs-lookup"><span data-stu-id="dcb48-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="dcb48-114">Det här kommandot konfigurerar DSC-tillägget på en virtuell dator med en sökväg till konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="dcb48-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="dcb48-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcb48-115">PARAMETERS</span></span>

### <span data-ttu-id="dcb48-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="dcb48-116">-ConfigurationArchive</span></span>
<span data-ttu-id="dcb48-117">Anger namnet på konfigurations paketet (zip-filen) som tidigare laddats upp av publicering-AzureVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dcb48-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="dcb48-118">Den här parametern får bara ange namnet på filen, utan sökväg.</span><span class="sxs-lookup"><span data-stu-id="dcb48-118">This parameter must specify only the name of the file, without any path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="dcb48-119">-ConfigurationArgument</span></span>
<span data-ttu-id="dcb48-120">Anger en hash-värde som anger argumenten för konfigurations funktionen.</span><span class="sxs-lookup"><span data-stu-id="dcb48-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="dcb48-121">Nycklarna motsvarar parameter namnen och värdena till parameter värdena.</span><span class="sxs-lookup"><span data-stu-id="dcb48-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="dcb48-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dcb48-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dcb48-123">primitiva typer</span><span class="sxs-lookup"><span data-stu-id="dcb48-123">primitive types</span></span>
- <span data-ttu-id="dcb48-124">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="dcb48-124">string</span></span>
- <span data-ttu-id="dcb48-125">enheter</span><span class="sxs-lookup"><span data-stu-id="dcb48-125">array</span></span>
- <span data-ttu-id="dcb48-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="dcb48-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="dcb48-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="dcb48-128">Anger sökvägen till en. psd1-fil som anger data för konfigurations funktionen.</span><span class="sxs-lookup"><span data-stu-id="dcb48-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="dcb48-129">Denna fil måste innehålla en hash-tabell enligt beskrivningen i avgränsa konfigurations-och miljö data https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="dcb48-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="dcb48-130">-ConfigurationName</span></span>
<span data-ttu-id="dcb48-131">Anger namnet på det konfigurations skript eller den modul som anropas av DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="dcb48-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="dcb48-132">Värdet för den här parametern måste vara namnet på en av konfigurations funktionerna som finns i skript eller moduler som är paketerade i *ConfigurationArchive*.</span><span class="sxs-lookup"><span data-stu-id="dcb48-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="dcb48-133">Denna cmdlet är standardvärdet för namnet på filen som anges med parametern *ConfigurationArchive* om du utelämnar den här parametern, exklusive alla tillägg.</span><span class="sxs-lookup"><span data-stu-id="dcb48-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="dcb48-134">Om *ConfigurationArchive* är "SalesWebSite.ps1.zip" är standardvärdet för *ConfigurationName* "SalesWebSite".</span><span class="sxs-lookup"><span data-stu-id="dcb48-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-135">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dcb48-135">-ContainerName</span></span>
<span data-ttu-id="dcb48-136">Anger namnet på den Azure Storage-behållare där *ConfigurationArchive* finns.</span><span class="sxs-lookup"><span data-stu-id="dcb48-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="dcb48-137">-DataCollection</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-138">-Force</span><span class="sxs-lookup"><span data-stu-id="dcb48-138">-Force</span></span>
<span data-ttu-id="dcb48-139">Anger att den här cmdleten skriver över befintliga blobs.</span><span class="sxs-lookup"><span data-stu-id="dcb48-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dcb48-140">-InformationAction</span></span>
<span data-ttu-id="dcb48-141">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="dcb48-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dcb48-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dcb48-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dcb48-143">Vidare</span><span class="sxs-lookup"><span data-stu-id="dcb48-143">Continue</span></span>
- <span data-ttu-id="dcb48-144">Över</span><span class="sxs-lookup"><span data-stu-id="dcb48-144">Ignore</span></span>
- <span data-ttu-id="dcb48-145">Inquire</span><span class="sxs-lookup"><span data-stu-id="dcb48-145">Inquire</span></span>
- <span data-ttu-id="dcb48-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dcb48-146">SilentlyContinue</span></span>
- <span data-ttu-id="dcb48-147">Stanna</span><span class="sxs-lookup"><span data-stu-id="dcb48-147">Stop</span></span>
- <span data-ttu-id="dcb48-148">Avbryt</span><span class="sxs-lookup"><span data-stu-id="dcb48-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dcb48-149">-InformationVariable</span></span>
<span data-ttu-id="dcb48-150">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="dcb48-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-151">-Profil</span><span class="sxs-lookup"><span data-stu-id="dcb48-151">-Profile</span></span>
<span data-ttu-id="dcb48-152">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="dcb48-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dcb48-153">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="dcb48-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-154">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="dcb48-154">-ReferenceName</span></span>
<span data-ttu-id="dcb48-155">Anger en användardefinierad sträng som kan användas för att referera till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="dcb48-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="dcb48-156">Den här parametern anges när tillägget läggs till på den virtuella datorn för första gången.</span><span class="sxs-lookup"><span data-stu-id="dcb48-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="dcb48-157">För kommande uppdateringar ska du ange det tidigare använda referens namnet medan du uppdaterar tillägget.</span><span class="sxs-lookup"><span data-stu-id="dcb48-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="dcb48-158">*ReferenceName* som tilldelats till ett tillägg returneras med cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="dcb48-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-159">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="dcb48-159">-StorageContext</span></span>
<span data-ttu-id="dcb48-160">Anger den Azure Storage-kontext som tillhandahåller de säkerhets inställningar som används för att komma åt konfigurations skriptet.</span><span class="sxs-lookup"><span data-stu-id="dcb48-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="dcb48-161">Den här kontexten ger Läs åtkomst till den behållare som anges av *ContainerName* -parametern.</span><span class="sxs-lookup"><span data-stu-id="dcb48-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcb48-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="dcb48-163">Anger DNS-slutpunktsmapparen för alla lagrings tjänster, till exempel "core.contoso.net".</span><span class="sxs-lookup"><span data-stu-id="dcb48-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-164">-Version</span><span class="sxs-lookup"><span data-stu-id="dcb48-164">-Version</span></span>
<span data-ttu-id="dcb48-165">Anger vilken version av DSC-tillägget som du vill använda.</span><span class="sxs-lookup"><span data-stu-id="dcb48-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="dcb48-166">Standardvärdet är "1. \*" om den här parametern inte anges.</span><span class="sxs-lookup"><span data-stu-id="dcb48-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-167">-VM</span><span class="sxs-lookup"><span data-stu-id="dcb48-167">-VM</span></span>
<span data-ttu-id="dcb48-168">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="dcb48-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="dcb48-169">-WmfVersion</span></span>
<span data-ttu-id="dcb48-170">Anger vilken version av Windows Management Framework (WMF) som ska installeras på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dcb48-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="dcb48-171">DSC-tillägget beror på DSC-funktioner som endast är tillgängliga i WMF-uppdateringarna.</span><span class="sxs-lookup"><span data-stu-id="dcb48-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="dcb48-172">Den här parametern anger vilken version av uppdateringen som ska installeras på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dcb48-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="dcb48-173">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dcb48-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dcb48-174">4,0.</span><span class="sxs-lookup"><span data-stu-id="dcb48-174">4.0.</span></span>
<span data-ttu-id="dcb48-175">Installerar WMF 4,0 såvida inte en nyare version redan är installerad.</span><span class="sxs-lookup"><span data-stu-id="dcb48-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="dcb48-176">5,0.</span><span class="sxs-lookup"><span data-stu-id="dcb48-176">5.0.</span></span>
<span data-ttu-id="dcb48-177">Installerar den senaste versionen av WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="dcb48-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="dcb48-178">RelatesTo.</span><span class="sxs-lookup"><span data-stu-id="dcb48-178">latest.</span></span>
<span data-ttu-id="dcb48-179">Installerar den senaste WMF-versionen för närvarande, WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="dcb48-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="dcb48-180">Standardvärdet är senaste.</span><span class="sxs-lookup"><span data-stu-id="dcb48-180">The default value is latest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dcb48-181">-Confirm</span></span>
<span data-ttu-id="dcb48-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dcb48-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcb48-183">-WhatIf</span></span>
<span data-ttu-id="dcb48-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dcb48-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcb48-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dcb48-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb48-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb48-186">CommonParameters</span></span>
<span data-ttu-id="dcb48-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcb48-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb48-188">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcb48-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb48-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcb48-189">INPUTS</span></span>

## <span data-ttu-id="dcb48-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcb48-190">OUTPUTS</span></span>

## <span data-ttu-id="dcb48-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcb48-191">NOTES</span></span>

## <span data-ttu-id="dcb48-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcb48-192">RELATED LINKS</span></span>

[<span data-ttu-id="dcb48-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dcb48-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="dcb48-194">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dcb48-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="dcb48-195">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="dcb48-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="dcb48-196">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="dcb48-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="dcb48-197">Publicera – AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcb48-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


