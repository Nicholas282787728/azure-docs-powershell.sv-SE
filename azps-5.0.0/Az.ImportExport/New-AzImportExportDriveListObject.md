---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270600"
---
# <span data-ttu-id="566ae-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="566ae-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="566ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="566ae-102">SYNOPSIS</span></span>
<span data-ttu-id="566ae-103">Skapa ett DriverList-objekt för ImportExport.</span><span class="sxs-lookup"><span data-stu-id="566ae-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="566ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="566ae-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="566ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="566ae-105">DESCRIPTION</span></span>
<span data-ttu-id="566ae-106">Skapa ett DriverList-objekt för ImportExport.</span><span class="sxs-lookup"><span data-stu-id="566ae-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="566ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="566ae-107">EXAMPLES</span></span>

### <span data-ttu-id="566ae-108">Exempel 1: skapa en ny DriveList för ImportExport-jobbet</span><span class="sxs-lookup"><span data-stu-id="566ae-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="566ae-109">Dessa cmdletar skapar en ny DriveList för ImportExport-jobb.</span><span class="sxs-lookup"><span data-stu-id="566ae-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="566ae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="566ae-110">PARAMETERS</span></span>

### <span data-ttu-id="566ae-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="566ae-111">-BitLockerKey</span></span>
<span data-ttu-id="566ae-112">Den BitLocker-nyckel som används för att kryptera enheten.</span><span class="sxs-lookup"><span data-stu-id="566ae-112">The BitLocker key used to encrypt the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="566ae-113">-BytesSucceeded</span></span>
<span data-ttu-id="566ae-114">Byte som lyckats överföras för enheten.</span><span class="sxs-lookup"><span data-stu-id="566ae-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="566ae-115">-CopyStatus</span></span>
<span data-ttu-id="566ae-116">Detaljerad status om data överförings processen.</span><span class="sxs-lookup"><span data-stu-id="566ae-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="566ae-117">Det här fältet returneras inte i svaret förrän enheten är i överförings läget.</span><span class="sxs-lookup"><span data-stu-id="566ae-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="566ae-118">-DriveHeaderHash</span></span>
<span data-ttu-id="566ae-119">Hash-värdet för enhetens huvud.</span><span class="sxs-lookup"><span data-stu-id="566ae-119">The drive header hash value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="566ae-120">-DriveId</span></span>
<span data-ttu-id="566ae-121">Enhetens serie nummer utan mellanslag.</span><span class="sxs-lookup"><span data-stu-id="566ae-121">The drive's hardware serial number, without spaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="566ae-122">-ErrorLogUri</span></span>
<span data-ttu-id="566ae-123">En URI som pekar på blobben som innehåller fel loggen för data överförings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="566ae-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="566ae-124">-ManifestFile</span></span>
<span data-ttu-id="566ae-125">Den relativa sökvägen till manifest filen på enheten.</span><span class="sxs-lookup"><span data-stu-id="566ae-125">The relative path of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="566ae-126">-ManifestHash</span></span>
<span data-ttu-id="566ae-127">Den Base16iska MD5-hashen för manifest filen på enheten.</span><span class="sxs-lookup"><span data-stu-id="566ae-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="566ae-128">-ManifestUri</span></span>
<span data-ttu-id="566ae-129">En URI som pekar på blobben som innehåller enhetens manifest fil.</span><span class="sxs-lookup"><span data-stu-id="566ae-129">A URI that points to the blob containing the drive manifest file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-130">-Procent färdigt</span><span class="sxs-lookup"><span data-stu-id="566ae-130">-PercentComplete</span></span>
<span data-ttu-id="566ae-131">Procent färdigt för enheten.</span><span class="sxs-lookup"><span data-stu-id="566ae-131">Percentage completed for the drive.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-132">-State</span><span class="sxs-lookup"><span data-stu-id="566ae-132">-State</span></span>
<span data-ttu-id="566ae-133">Enhetens aktuella status.</span><span class="sxs-lookup"><span data-stu-id="566ae-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="566ae-134">-VerboseLogUri</span></span>
<span data-ttu-id="566ae-135">En URI som pekar på blobben som innehåller utförlig loggen för data överförings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="566ae-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566ae-136">CommonParameters</span></span>
<span data-ttu-id="566ae-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="566ae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566ae-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="566ae-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566ae-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="566ae-139">INPUTS</span></span>

## <span data-ttu-id="566ae-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="566ae-140">OUTPUTS</span></span>

### <span data-ttu-id="566ae-141">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. Api20161101. IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="566ae-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="566ae-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="566ae-142">NOTES</span></span>

<span data-ttu-id="566ae-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="566ae-143">ALIASES</span></span>

## <span data-ttu-id="566ae-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="566ae-144">RELATED LINKS</span></span>
