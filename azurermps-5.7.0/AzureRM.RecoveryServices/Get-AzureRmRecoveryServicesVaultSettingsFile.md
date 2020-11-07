---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b272f22c0bac37f5318deff50f1f0b56a849ce2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756788"
---
# <span data-ttu-id="7ae16-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7ae16-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="7ae16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ae16-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae16-103">Hämtar inställningar för Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="7ae16-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ae16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ae16-104">SYNTAX</span></span>

### <span data-ttu-id="7ae16-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="7ae16-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ae16-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="7ae16-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ae16-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="7ae16-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ae16-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ae16-108">DESCRIPTION</span></span>
<span data-ttu-id="7ae16-109">Cmdleten **Get-AzureRmRecoveryServicesVaultSettingsFile** hämtar inställnings filen för ett Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="7ae16-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7ae16-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ae16-110">EXAMPLES</span></span>

### <span data-ttu-id="7ae16-111">Exempel 1: registrera en Windows Server eller DPM-dator för Azure-säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="7ae16-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="7ae16-112">Det första kommandot får valvet med namnet TestVault och lagrar det sedan i variabeln $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="7ae16-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="7ae16-113">Det andra kommandot anger $CredsPath variabeln till C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="7ae16-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="7ae16-114">Det sista kommandot får valv filen för autentiseringsuppgifter för $Vault 01 genom att använda autentiseringsuppgifterna i $CredsPath för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="7ae16-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="7ae16-115">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="7ae16-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="7ae16-116">Kommandot hämtar valvets autentiseringsinformation för $Vault 01 siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="7ae16-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="7ae16-117">Exempel 3: registrera en Windows Server eller DPM-dator för Azure-säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="7ae16-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="7ae16-118">Kommandot hämtar valv filen för autentiseringsuppgifter för $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="7ae16-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="7ae16-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ae16-119">PARAMETERS</span></span>

### <span data-ttu-id="7ae16-120">-Säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="7ae16-120">-Backup</span></span>
<span data-ttu-id="7ae16-121">Anger att valvets autentiseringsinformation är tillämpbar för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="7ae16-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae16-122">-Path</span><span class="sxs-lookup"><span data-stu-id="7ae16-122">-Path</span></span>
<span data-ttu-id="7ae16-123">Anger sökvägen till inställnings filen för Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="7ae16-123">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="7ae16-124">Du kan ladda ned filen från portalen för Azure Site Recovery Vault och lagra den lokalt.</span><span class="sxs-lookup"><span data-stu-id="7ae16-124">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae16-125">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7ae16-125">-SiteFriendlyName</span></span>
<span data-ttu-id="7ae16-126">Anger det eget namn för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="7ae16-126">Specifies the site friendly name.</span></span>
<span data-ttu-id="7ae16-127">Använd den här parametern om du hämtar valv-autentiseringsuppgifterna för en Hyper-V-webbplats.</span><span class="sxs-lookup"><span data-stu-id="7ae16-127">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae16-128">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="7ae16-128">-SiteIdentifier</span></span>
<span data-ttu-id="7ae16-129">Anger webbplats-ID.</span><span class="sxs-lookup"><span data-stu-id="7ae16-129">Specifies the site identifier.</span></span>
<span data-ttu-id="7ae16-130">Använd den här parametern om du hämtar valv-autentiseringsuppgifterna för en Hyper-V-webbplats.</span><span class="sxs-lookup"><span data-stu-id="7ae16-130">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae16-131">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7ae16-131">-SiteRecovery</span></span>
<span data-ttu-id="7ae16-132">Anger att valv filen för valvet är tillämplig på Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7ae16-132">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae16-133">-Valv</span><span class="sxs-lookup"><span data-stu-id="7ae16-133">-Vault</span></span>
<span data-ttu-id="7ae16-134">Anger Azure Site Recovery-valv objekt.</span><span class="sxs-lookup"><span data-stu-id="7ae16-134">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae16-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae16-135">-DefaultProfile</span></span>
<span data-ttu-id="7ae16-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae16-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae16-137">CommonParameters</span></span>
<span data-ttu-id="7ae16-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae16-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae16-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae16-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ae16-140">INPUTS</span></span>

### <span data-ttu-id="7ae16-141">ARSVault</span><span class="sxs-lookup"><span data-stu-id="7ae16-141">ARSVault</span></span>
<span data-ttu-id="7ae16-142">Parametern ' valv ' godkänner värdet av typen ' ARSVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7ae16-142">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="7ae16-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ae16-143">OUTPUTS</span></span>

### <span data-ttu-id="7ae16-144">Microsoft. Azure. commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="7ae16-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="7ae16-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ae16-145">NOTES</span></span>

## <span data-ttu-id="7ae16-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ae16-146">RELATED LINKS</span></span>

[<span data-ttu-id="7ae16-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7ae16-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7ae16-148">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7ae16-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7ae16-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7ae16-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


