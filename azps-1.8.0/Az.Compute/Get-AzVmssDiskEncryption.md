---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5219b43a1d80515f0bce02c5f6fdd2117b736a00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754562"
---
# <span data-ttu-id="aa0e5-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="aa0e5-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="aa0e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0e5-103">Visar disk krypterings statusen för en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="aa0e5-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="aa0e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa0e5-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa0e5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa0e5-105">DESCRIPTION</span></span>
<span data-ttu-id="aa0e5-106">Visar disk krypterings statusen för en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="aa0e5-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="aa0e5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa0e5-107">EXAMPLES</span></span>

### <span data-ttu-id="aa0e5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aa0e5-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="aa0e5-109">Visar disk krypterings statusen för den virtuella datorns skalnings uppsättning med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="aa0e5-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="aa0e5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa0e5-110">PARAMETERS</span></span>

### <span data-ttu-id="aa0e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0e5-111">-DefaultProfile</span></span>
<span data-ttu-id="aa0e5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aa0e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa0e5-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="aa0e5-113">-ExtensionName</span></span>
<span data-ttu-id="aa0e5-114">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="aa0e5-114">The extension name.</span></span>
<span data-ttu-id="aa0e5-115">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="aa0e5-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0e5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0e5-116">-ResourceGroupName</span></span>
<span data-ttu-id="aa0e5-117">Resurs grupp namn för den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="aa0e5-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="aa0e5-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="aa0e5-118">-VMScaleSetName</span></span>
<span data-ttu-id="aa0e5-119">Den virtuella datorns skal uppsättnings namn.</span><span class="sxs-lookup"><span data-stu-id="aa0e5-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0e5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0e5-120">CommonParameters</span></span>
<span data-ttu-id="aa0e5-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa0e5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0e5-122">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa0e5-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0e5-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa0e5-123">INPUTS</span></span>

### <span data-ttu-id="aa0e5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="aa0e5-124">System.String</span></span>

## <span data-ttu-id="aa0e5-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa0e5-125">OUTPUTS</span></span>

### <span data-ttu-id="aa0e5-126">Microsoft. Azure. commands. Compute. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="aa0e5-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="aa0e5-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa0e5-127">NOTES</span></span>

## <span data-ttu-id="aa0e5-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa0e5-128">RELATED LINKS</span></span>
