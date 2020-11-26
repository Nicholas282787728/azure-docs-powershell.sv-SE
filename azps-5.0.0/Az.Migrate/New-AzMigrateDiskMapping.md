---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272099"
---
# <span data-ttu-id="391cd-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="391cd-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="391cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="391cd-102">SYNOPSIS</span></span>
<span data-ttu-id="391cd-103">Skapar en ny disk mappning</span><span class="sxs-lookup"><span data-stu-id="391cd-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="391cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="391cd-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="391cd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="391cd-105">DESCRIPTION</span></span>
<span data-ttu-id="391cd-106">New-AzMigrateDiskMapping-cmdleten skapar en mappning av käll disken som är ansluten till servern som ska migreras</span><span class="sxs-lookup"><span data-stu-id="391cd-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="391cd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="391cd-107">EXAMPLES</span></span>

### <span data-ttu-id="391cd-108">Exempel 1: skapa diskar</span><span class="sxs-lookup"><span data-stu-id="391cd-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="391cd-109">Ladda ner diskar för att ange indata för New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="391cd-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="391cd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="391cd-110">PARAMETERS</span></span>

### <span data-ttu-id="391cd-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="391cd-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="391cd-112">Anger vilken encyption som ska användas.</span><span class="sxs-lookup"><span data-stu-id="391cd-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="391cd-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="391cd-113">-DiskID</span></span>
<span data-ttu-id="391cd-114">Anger disk-ID för den disk som är ansluten till den upptäckta server som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="391cd-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391cd-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="391cd-115">-DiskType</span></span>
<span data-ttu-id="391cd-116">Anger vilken typ av disk som ska användas för Azure VM.</span><span class="sxs-lookup"><span data-stu-id="391cd-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391cd-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="391cd-117">-IsOSDisk</span></span>
<span data-ttu-id="391cd-118">Anger om disken innehåller operativ systemet för käll servern som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="391cd-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391cd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391cd-119">CommonParameters</span></span>
<span data-ttu-id="391cd-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="391cd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391cd-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="391cd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391cd-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="391cd-122">INPUTS</span></span>

## <span data-ttu-id="391cd-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="391cd-123">OUTPUTS</span></span>

### <span data-ttu-id="391cd-124">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="391cd-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="391cd-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="391cd-125">NOTES</span></span>

<span data-ttu-id="391cd-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="391cd-126">ALIASES</span></span>

## <span data-ttu-id="391cd-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="391cd-127">RELATED LINKS</span></span>
