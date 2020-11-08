---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 844808f541c5ac04d7c27a140da1aa1d39fe439d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925126"
---
# <span data-ttu-id="69814-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="69814-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="69814-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69814-102">SYNOPSIS</span></span>
<span data-ttu-id="69814-103">Visar disk krypterings statusen för en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="69814-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="69814-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69814-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69814-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69814-105">DESCRIPTION</span></span>
<span data-ttu-id="69814-106">Visar disk krypterings statusen för en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="69814-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="69814-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69814-107">EXAMPLES</span></span>

### <span data-ttu-id="69814-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69814-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="69814-109">Visar disk krypterings statusen för den virtuella datorns skalnings uppsättning med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="69814-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="69814-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69814-110">PARAMETERS</span></span>

### <span data-ttu-id="69814-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69814-111">-DefaultProfile</span></span>
<span data-ttu-id="69814-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69814-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69814-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="69814-113">-ExtensionName</span></span>
<span data-ttu-id="69814-114">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="69814-114">The extension name.</span></span>
<span data-ttu-id="69814-115">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="69814-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69814-116">-ResourceGroupName</span></span>
<span data-ttu-id="69814-117">Resurs grupp namn för den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="69814-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="69814-118">-VMScaleSetName</span></span>
<span data-ttu-id="69814-119">Den virtuella datorns skal uppsättnings namn.</span><span class="sxs-lookup"><span data-stu-id="69814-119">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69814-120">CommonParameters</span></span>
<span data-ttu-id="69814-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69814-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69814-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69814-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69814-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69814-123">INPUTS</span></span>

### <span data-ttu-id="69814-124">System. String</span><span class="sxs-lookup"><span data-stu-id="69814-124">System.String</span></span>

## <span data-ttu-id="69814-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69814-125">OUTPUTS</span></span>

### <span data-ttu-id="69814-126">Microsoft. Azure. commands. Compute. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="69814-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="69814-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69814-127">NOTES</span></span>

## <span data-ttu-id="69814-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69814-128">RELATED LINKS</span></span>
