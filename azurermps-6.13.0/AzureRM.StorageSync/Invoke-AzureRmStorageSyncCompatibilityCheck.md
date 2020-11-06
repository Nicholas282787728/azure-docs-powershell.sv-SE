---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578707"
---
# <span data-ttu-id="17049-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="17049-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="17049-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17049-102">SYNOPSIS</span></span>
<span data-ttu-id="17049-103">Kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="17049-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17049-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17049-104">SYNTAX</span></span>

### <span data-ttu-id="17049-105">PathBased (standard)</span><span class="sxs-lookup"><span data-stu-id="17049-105">PathBased (Default)</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### <span data-ttu-id="17049-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="17049-106">ComputerNameBased</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## <span data-ttu-id="17049-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17049-107">DESCRIPTION</span></span>
<span data-ttu-id="17049-108">Cmdleten **Invoke-AzureRmStorageSyncCompatibilityCheck** kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering. Med en lokal eller fjärrsökväg utför den en uppsättning valideringar på systemet och fil namn rymden och returnerar sedan eventuella kompatibilitetsproblem som hittas.</span><span class="sxs-lookup"><span data-stu-id="17049-108">The **Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="17049-109">System kontroller:</span><span class="sxs-lookup"><span data-stu-id="17049-109">System checks:</span></span>
- <span data-ttu-id="17049-110">Fil namns namnrymd för webbläsarkompatibilitet kontrollerar:</span><span class="sxs-lookup"><span data-stu-id="17049-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="17049-111">Tecken som inte stöds</span><span class="sxs-lookup"><span data-stu-id="17049-111">Unsupported characters</span></span>
- <span data-ttu-id="17049-112">Maximal fil storlek</span><span class="sxs-lookup"><span data-stu-id="17049-112">Maximum file size</span></span>
- <span data-ttu-id="17049-113">Maximal Sök vägs längd</span><span class="sxs-lookup"><span data-stu-id="17049-113">Maximum path length</span></span>
- <span data-ttu-id="17049-114">Maximal fil längd</span><span class="sxs-lookup"><span data-stu-id="17049-114">Maximum file length</span></span>
- <span data-ttu-id="17049-115">Maximal mängd storlek</span><span class="sxs-lookup"><span data-stu-id="17049-115">Maximum dataset size</span></span>
- <span data-ttu-id="17049-116">Maximalt katalog djup</span><span class="sxs-lookup"><span data-stu-id="17049-116">Maximum directory depth</span></span>

## <span data-ttu-id="17049-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17049-117">EXAMPLES</span></span>

### <span data-ttu-id="17049-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17049-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="17049-119">Det här kommandot kontrollerar kompatibiliteten för systemet och även filer och mappar i C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="17049-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="17049-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="17049-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="17049-121">Det här kommandot kontrollerar kompatibiliteten för filer och mappar i C:\DATA, men utför ingen kompatibilitetskontroll.</span><span class="sxs-lookup"><span data-stu-id="17049-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="17049-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="17049-122">Example 3</span></span>
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

<span data-ttu-id="17049-123">Det här kommandot kontrollerar kompatibiliteten för systemet och även filer och mappar i C:\DATA och exporterar sedan resultaten som en CSV-fil till C:\results.</span><span class="sxs-lookup"><span data-stu-id="17049-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="17049-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17049-124">PARAMETERS</span></span>

### <span data-ttu-id="17049-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="17049-125">-ComputerName</span></span>
<span data-ttu-id="17049-126">Den dator där du utför den här kontrollen.</span><span class="sxs-lookup"><span data-stu-id="17049-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17049-127">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="17049-127">-Credential</span></span>
<span data-ttu-id="17049-128">Dina autentiseringsuppgifter för den delning du verifierar.</span><span class="sxs-lookup"><span data-stu-id="17049-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17049-129">-Path</span><span class="sxs-lookup"><span data-stu-id="17049-129">-Path</span></span>
<span data-ttu-id="17049-130">UNC-sökvägen för den resurs som du verifierar.</span><span class="sxs-lookup"><span data-stu-id="17049-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17049-131">-Quiet</span><span class="sxs-lookup"><span data-stu-id="17049-131">-Quiet</span></span>
<span data-ttu-id="17049-132">Utelämnar Skriv ut rapport till konsol.</span><span class="sxs-lookup"><span data-stu-id="17049-132">Suppresses writing output report to console.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17049-133">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="17049-133">-SkipNamespaceChecks</span></span>
<span data-ttu-id="17049-134">Ange den här flaggan för att hoppa över valideringar av fil namn områden och endast utföra system verifieringar.</span><span class="sxs-lookup"><span data-stu-id="17049-134">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17049-135">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="17049-135">-SkipSystemChecks</span></span>
<span data-ttu-id="17049-136">Ange den här flaggan för att hoppa över system verifieringar och endast utföra verifieringar av fil namn.</span><span class="sxs-lookup"><span data-stu-id="17049-136">Set this flag to skip system validations and only perform file namespace validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17049-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17049-137">CommonParameters</span></span>
<span data-ttu-id="17049-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17049-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17049-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17049-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17049-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17049-140">INPUTS</span></span>

### <span data-ttu-id="17049-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="17049-141">None</span></span>

## <span data-ttu-id="17049-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17049-142">OUTPUTS</span></span>

### <span data-ttu-id="17049-143">Microsoft. Azure. commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="17049-143">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="17049-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17049-144">NOTES</span></span>
* <span data-ttu-id="17049-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, storagesync, FileSync</span><span class="sxs-lookup"><span data-stu-id="17049-145">Keywords: azure, azurerm, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="17049-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17049-146">RELATED LINKS</span></span>
