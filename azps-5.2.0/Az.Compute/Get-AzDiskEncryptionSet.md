---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392987"
---
# <span data-ttu-id="37c5f-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="37c5f-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="37c5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="37c5f-103">Hämta eller Visa disk krypterings uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="37c5f-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="37c5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37c5f-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37c5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="37c5f-106">Hämta eller Visa disk krypterings uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="37c5f-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="37c5f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37c5f-107">EXAMPLES</span></span>

### <span data-ttu-id="37c5f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="37c5f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="37c5f-109">Hämta disk krypterings uppsättning ' enc1 '</span><span class="sxs-lookup"><span data-stu-id="37c5f-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="37c5f-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="37c5f-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="37c5f-111">Hämta alla disk krypterings uppsättningar i resurs gruppen ' RG1 '.</span><span class="sxs-lookup"><span data-stu-id="37c5f-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="37c5f-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="37c5f-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="37c5f-113">Hämta alla disk krypterings uppsättningar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="37c5f-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="37c5f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37c5f-114">PARAMETERS</span></span>

### <span data-ttu-id="37c5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c5f-115">-DefaultProfile</span></span>
<span data-ttu-id="37c5f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37c5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c5f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="37c5f-117">-Name</span></span>
<span data-ttu-id="37c5f-118">Namn på disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="37c5f-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37c5f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c5f-119">-ResourceGroupName</span></span>
<span data-ttu-id="37c5f-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="37c5f-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37c5f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c5f-121">CommonParameters</span></span>
<span data-ttu-id="37c5f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c5f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c5f-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37c5f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c5f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37c5f-124">INPUTS</span></span>

### <span data-ttu-id="37c5f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="37c5f-125">System.String</span></span>

## <span data-ttu-id="37c5f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37c5f-126">OUTPUTS</span></span>

### <span data-ttu-id="37c5f-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="37c5f-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="37c5f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37c5f-128">NOTES</span></span>

## <span data-ttu-id="37c5f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37c5f-129">RELATED LINKS</span></span>
