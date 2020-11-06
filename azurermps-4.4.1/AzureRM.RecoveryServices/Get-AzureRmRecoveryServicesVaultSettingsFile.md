---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582235"
---
# <span data-ttu-id="b87e6-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b87e6-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="b87e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b87e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b87e6-103">Hämtar inställningar för Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="b87e6-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b87e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b87e6-104">SYNTAX</span></span>

### <span data-ttu-id="b87e6-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="b87e6-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b87e6-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="b87e6-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b87e6-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="b87e6-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b87e6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b87e6-108">DESCRIPTION</span></span>
<span data-ttu-id="b87e6-109">Cmdleten **Get-AzureRmRecoveryServicesVaultSettingsFile** hämtar inställnings filen för ett Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="b87e6-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b87e6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b87e6-110">EXAMPLES</span></span>

### <span data-ttu-id="b87e6-111">Exempel 1: registrera en Windows Server eller DPM-dator för Azure-säkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="b87e6-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="b87e6-112">Det första kommandot får valvet med namnet TestVault och lagrar det sedan i variabeln $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="b87e6-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="b87e6-113">Det andra kommandot anger $CredsPath variabeln till C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="b87e6-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="b87e6-114">Det sista kommandot får valv filen för autentiseringsuppgifter för $Vault 01 genom att använda autentiseringsuppgifterna i $CredsPath för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="b87e6-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="b87e6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b87e6-115">PARAMETERS</span></span>

### <span data-ttu-id="b87e6-116">-Säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="b87e6-116">-Backup</span></span>
<span data-ttu-id="b87e6-117">Anger att valvets autentiseringsinformation är tillämpbar för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="b87e6-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87e6-118">-Path</span><span class="sxs-lookup"><span data-stu-id="b87e6-118">-Path</span></span>
<span data-ttu-id="b87e6-119">Anger sökvägen till inställnings filen för Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="b87e6-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="b87e6-120">Du kan ladda ned filen från portalen för Azure Site Recovery Vault och lagra den lokalt.</span><span class="sxs-lookup"><span data-stu-id="b87e6-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87e6-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b87e6-121">-SiteFriendlyName</span></span>
<span data-ttu-id="b87e6-122">Anger det eget namn för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="b87e6-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="b87e6-123">Använd den här parametern om du hämtar valv-autentiseringsuppgifterna för en Hyper-V-webbplats.</span><span class="sxs-lookup"><span data-stu-id="b87e6-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87e6-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="b87e6-124">-SiteIdentifier</span></span>
<span data-ttu-id="b87e6-125">Anger webbplats-ID.</span><span class="sxs-lookup"><span data-stu-id="b87e6-125">Specifies the site identifier.</span></span>
<span data-ttu-id="b87e6-126">Använd den här parametern om du hämtar valv-autentiseringsuppgifterna för en Hyper-V-webbplats.</span><span class="sxs-lookup"><span data-stu-id="b87e6-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87e6-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b87e6-127">-SiteRecovery</span></span>
<span data-ttu-id="b87e6-128">Anger att valv filen för valvet är tillämplig på Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b87e6-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87e6-129">-Valv</span><span class="sxs-lookup"><span data-stu-id="b87e6-129">-Vault</span></span>
<span data-ttu-id="b87e6-130">Anger Azure Site Recovery-valv objekt.</span><span class="sxs-lookup"><span data-stu-id="b87e6-130">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b87e6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b87e6-131">-DefaultProfile</span></span>
<span data-ttu-id="b87e6-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b87e6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b87e6-133">CommonParameters</span></span>
<span data-ttu-id="b87e6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b87e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b87e6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b87e6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b87e6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b87e6-136">INPUTS</span></span>

### <span data-ttu-id="b87e6-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="b87e6-137">ARSVault</span></span>
<span data-ttu-id="b87e6-138">Parametern ' valv ' godkänner värdet av typen ' ARSVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b87e6-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="b87e6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b87e6-139">OUTPUTS</span></span>

### <span data-ttu-id="b87e6-140">Microsoft. Azure. commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="b87e6-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="b87e6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b87e6-141">NOTES</span></span>

## <span data-ttu-id="b87e6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b87e6-142">RELATED LINKS</span></span>

[<span data-ttu-id="b87e6-143">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b87e6-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="b87e6-144">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b87e6-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="b87e6-145">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b87e6-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


