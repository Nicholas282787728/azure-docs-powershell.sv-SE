---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324804"
---
# <span data-ttu-id="74c64-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="74c64-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="74c64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74c64-102">SYNOPSIS</span></span>
<span data-ttu-id="74c64-103">Hämtar listan över resurser som är kopplade till den angivna disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="74c64-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="74c64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74c64-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74c64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74c64-105">DESCRIPTION</span></span>
<span data-ttu-id="74c64-106">Cmdleten **Get-AzDiskEncryptionSetAssociatedResource** hämtar listan över resurser som är kopplade till den angivna disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="74c64-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="74c64-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74c64-107">EXAMPLES</span></span>

### <span data-ttu-id="74c64-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="74c64-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="74c64-109">Cmdleten hämtar de två resurserna, "exampleDisk01" och "exampleDisk02", associerade med angiven disk krypterings uppsättning</span><span class="sxs-lookup"><span data-stu-id="74c64-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="74c64-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74c64-110">PARAMETERS</span></span>

### <span data-ttu-id="74c64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c64-111">-DefaultProfile</span></span>
<span data-ttu-id="74c64-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74c64-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74c64-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="74c64-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="74c64-114">Namn på disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="74c64-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c64-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c64-115">-ResourceGroupName</span></span>
<span data-ttu-id="74c64-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="74c64-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c64-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c64-117">CommonParameters</span></span>
<span data-ttu-id="74c64-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c64-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c64-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74c64-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c64-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74c64-120">INPUTS</span></span>

### <span data-ttu-id="74c64-121">System. String</span><span class="sxs-lookup"><span data-stu-id="74c64-121">System.String</span></span>

## <span data-ttu-id="74c64-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74c64-122">OUTPUTS</span></span>

### <span data-ttu-id="74c64-123">System. URI []</span><span class="sxs-lookup"><span data-stu-id="74c64-123">System.Uri[]</span></span>

## <span data-ttu-id="74c64-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74c64-124">NOTES</span></span>

## <span data-ttu-id="74c64-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74c64-125">RELATED LINKS</span></span>