---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: c49fc472c6cc3693145487bdfe7488d0eabfe237
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929953"
---
# <span data-ttu-id="9a2bf-101">Get-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9a2bf-101">Get-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="9a2bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="9a2bf-103">Visar disk krypterings statusen för en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="9a2bf-103">Shows the disk encryption status of a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a2bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a2bf-104">SYNTAX</span></span>

```
Get-AzureRmVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a2bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a2bf-105">DESCRIPTION</span></span>
<span data-ttu-id="9a2bf-106">Visar disk krypterings statusen för en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="9a2bf-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="9a2bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a2bf-107">EXAMPLES</span></span>

### <span data-ttu-id="9a2bf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a2bf-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="9a2bf-109">Visar disk krypterings statusen för den virtuella datorns skalnings uppsättning med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="9a2bf-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="9a2bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a2bf-110">PARAMETERS</span></span>

### <span data-ttu-id="9a2bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a2bf-111">-DefaultProfile</span></span>
<span data-ttu-id="9a2bf-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a2bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a2bf-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="9a2bf-113">-ExtensionName</span></span>
<span data-ttu-id="9a2bf-114">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="9a2bf-114">The extension name.</span></span>
<span data-ttu-id="9a2bf-115">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="9a2bf-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="9a2bf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a2bf-116">-ResourceGroupName</span></span>
<span data-ttu-id="9a2bf-117">Resurs grupp namn för den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="9a2bf-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="9a2bf-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9a2bf-118">-VMScaleSetName</span></span>
<span data-ttu-id="9a2bf-119">Den virtuella datorns skal uppsättnings namn.</span><span class="sxs-lookup"><span data-stu-id="9a2bf-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="9a2bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a2bf-120">CommonParameters</span></span>
<span data-ttu-id="9a2bf-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a2bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a2bf-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a2bf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a2bf-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a2bf-123">INPUTS</span></span>

### <span data-ttu-id="9a2bf-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9a2bf-124">System.String</span></span>

## <span data-ttu-id="9a2bf-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a2bf-125">OUTPUTS</span></span>

### <span data-ttu-id="9a2bf-126">Microsoft. Azure. commands. Compute. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="9a2bf-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="9a2bf-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a2bf-127">NOTES</span></span>

## <span data-ttu-id="9a2bf-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a2bf-128">RELATED LINKS</span></span>
