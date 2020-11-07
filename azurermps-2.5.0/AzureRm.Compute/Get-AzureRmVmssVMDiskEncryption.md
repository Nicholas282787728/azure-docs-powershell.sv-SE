---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
ms.openlocfilehash: 41c18a3f9b1536e837ab8e127bfe00b62c74b5e1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931041"
---
# <span data-ttu-id="d1896-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d1896-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="d1896-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1896-102">SYNOPSIS</span></span>
<span data-ttu-id="d1896-103">Visar disk krypterings statusen för virtuella datorer i en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="d1896-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1896-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1896-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1896-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1896-105">DESCRIPTION</span></span>
<span data-ttu-id="d1896-106">Visar disk krypterings statusen för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d1896-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="d1896-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1896-107">EXAMPLES</span></span>

### <span data-ttu-id="d1896-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1896-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="d1896-109">Visar disk krypterings statusen för VM instans 1 i den virtuella datorns skal uppsättning med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="d1896-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="d1896-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1896-110">PARAMETERS</span></span>

### <span data-ttu-id="d1896-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1896-111">-DefaultProfile</span></span>
<span data-ttu-id="d1896-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1896-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1896-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="d1896-113">-ExtensionName</span></span>
<span data-ttu-id="d1896-114">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="d1896-114">The extension name.</span></span>
<span data-ttu-id="d1896-115">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="d1896-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1896-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d1896-116">-InstanceId</span></span>
<span data-ttu-id="d1896-117">Anger instans-ID.</span><span class="sxs-lookup"><span data-stu-id="d1896-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="d1896-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1896-118">-ResourceGroupName</span></span>
<span data-ttu-id="d1896-119">Resurs grupp namn för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d1896-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d1896-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d1896-120">-VMScaleSetName</span></span>
<span data-ttu-id="d1896-121">Den virtuella datorns skal uppsättnings namn.</span><span class="sxs-lookup"><span data-stu-id="d1896-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="d1896-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1896-122">CommonParameters</span></span>
<span data-ttu-id="d1896-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1896-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1896-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1896-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1896-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1896-125">INPUTS</span></span>

### <span data-ttu-id="d1896-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d1896-126">System.String</span></span>

## <span data-ttu-id="d1896-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1896-127">OUTPUTS</span></span>

### <span data-ttu-id="d1896-128">Microsoft. Azure. commands. Compute. Models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="d1896-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="d1896-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1896-129">NOTES</span></span>

## <span data-ttu-id="d1896-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1896-130">RELATED LINKS</span></span>

