---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261509"
---
# <span data-ttu-id="dbff3-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="dbff3-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="dbff3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbff3-102">SYNOPSIS</span></span>
<span data-ttu-id="dbff3-103">Kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering.</span><span class="sxs-lookup"><span data-stu-id="dbff3-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="dbff3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbff3-104">SYNTAX</span></span>

### <span data-ttu-id="dbff3-105">PathBased (standard)</span><span class="sxs-lookup"><span data-stu-id="dbff3-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="dbff3-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="dbff3-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="dbff3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbff3-107">DESCRIPTION</span></span>
<span data-ttu-id="dbff3-108">Cmdleten **Invoke-AzStorageSyncCompatibilityCheck** kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering. Med en lokal eller fjärrsökväg utför den en uppsättning valideringar på systemet och fil namn rymden och returnerar sedan eventuella kompatibilitetsproblem som hittas.</span><span class="sxs-lookup"><span data-stu-id="dbff3-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="dbff3-109">System kontroller:</span><span class="sxs-lookup"><span data-stu-id="dbff3-109">System checks:</span></span>
- <span data-ttu-id="dbff3-110">Fil namns namnrymd för webbläsarkompatibilitet kontrollerar:</span><span class="sxs-lookup"><span data-stu-id="dbff3-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="dbff3-111">Tecken som inte stöds</span><span class="sxs-lookup"><span data-stu-id="dbff3-111">Unsupported characters</span></span>
- <span data-ttu-id="dbff3-112">Maximal fil storlek</span><span class="sxs-lookup"><span data-stu-id="dbff3-112">Maximum file size</span></span>
- <span data-ttu-id="dbff3-113">Maximal Sök vägs längd</span><span class="sxs-lookup"><span data-stu-id="dbff3-113">Maximum path length</span></span>
- <span data-ttu-id="dbff3-114">Maximal fil längd</span><span class="sxs-lookup"><span data-stu-id="dbff3-114">Maximum file length</span></span>
- <span data-ttu-id="dbff3-115">Maximal mängd storlek</span><span class="sxs-lookup"><span data-stu-id="dbff3-115">Maximum dataset size</span></span>
- <span data-ttu-id="dbff3-116">Maximalt katalog djup</span><span class="sxs-lookup"><span data-stu-id="dbff3-116">Maximum directory depth</span></span>

## <span data-ttu-id="dbff3-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbff3-117">EXAMPLES</span></span>

### <span data-ttu-id="dbff3-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dbff3-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="dbff3-119">Det här kommandot kontrollerar kompatibiliteten för systemet och även filer och mappar i C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="dbff3-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="dbff3-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dbff3-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="dbff3-121">Det här kommandot kontrollerar kompatibiliteten för filer och mappar i C:\DATA, men utför ingen kompatibilitetskontroll.</span><span class="sxs-lookup"><span data-stu-id="dbff3-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="dbff3-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="dbff3-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="dbff3-123">Det här kommandot kontrollerar kompatibiliteten för systemet och även filer och mappar i C:\DATA och exporterar sedan resultaten som en CSV-fil till C:\results.</span><span class="sxs-lookup"><span data-stu-id="dbff3-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="dbff3-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbff3-124">PARAMETERS</span></span>

### <span data-ttu-id="dbff3-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="dbff3-125">-ComputerName</span></span>
<span data-ttu-id="dbff3-126">Den dator där du utför den här kontrollen.</span><span class="sxs-lookup"><span data-stu-id="dbff3-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="dbff3-127">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="dbff3-127">-Credential</span></span>
<span data-ttu-id="dbff3-128">Dina autentiseringsuppgifter för den delning du verifierar.</span><span class="sxs-lookup"><span data-stu-id="dbff3-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="dbff3-129">-Path</span><span class="sxs-lookup"><span data-stu-id="dbff3-129">-Path</span></span>
<span data-ttu-id="dbff3-130">UNC-sökvägen för den resurs som du verifierar.</span><span class="sxs-lookup"><span data-stu-id="dbff3-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="dbff3-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="dbff3-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="dbff3-132">Ange den här flaggan för att hoppa över valideringar av fil namn områden och endast utföra system verifieringar.</span><span class="sxs-lookup"><span data-stu-id="dbff3-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="dbff3-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="dbff3-133">-SkipSystemChecks</span></span>
<span data-ttu-id="dbff3-134">Ange den här flaggan för att hoppa över system verifieringar och endast utföra verifieringar av fil namn.</span><span class="sxs-lookup"><span data-stu-id="dbff3-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="dbff3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbff3-135">CommonParameters</span></span>
<span data-ttu-id="dbff3-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbff3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbff3-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbff3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbff3-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbff3-138">INPUTS</span></span>

### <span data-ttu-id="dbff3-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="dbff3-139">None</span></span>

## <span data-ttu-id="dbff3-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbff3-140">OUTPUTS</span></span>

### <span data-ttu-id="dbff3-141">Microsoft. Azure. commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="dbff3-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="dbff3-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbff3-142">NOTES</span></span>
* <span data-ttu-id="dbff3-143">Nyckelord: Azure, AZ, arm, resurs, hantering, storagesync, FileSync</span><span class="sxs-lookup"><span data-stu-id="dbff3-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="dbff3-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbff3-144">RELATED LINKS</span></span>
