---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579607"
---
# <span data-ttu-id="57fff-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="57fff-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="57fff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57fff-102">SYNOPSIS</span></span>
<span data-ttu-id="57fff-103">Ändrar egenskaper för en data disk för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="57fff-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57fff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57fff-104">SYNTAX</span></span>

### <span data-ttu-id="57fff-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="57fff-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="57fff-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="57fff-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="57fff-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57fff-107">DESCRIPTION</span></span>
<span data-ttu-id="57fff-108">Cmdleten **set-AzureRmVMDataDisk** ändrar egenskaper för en virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="57fff-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="57fff-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57fff-109">EXAMPLES</span></span>

### <span data-ttu-id="57fff-110">Exempel 1: ändra cacheläge för en data disk</span><span class="sxs-lookup"><span data-stu-id="57fff-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="57fff-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="57fff-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="57fff-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="57fff-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="57fff-113">Det andra kommandot ändrar cacheläge för data disken med namnet DataDisk01 på den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="57fff-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="57fff-114">Kommandot skickar resultatet till Update-AzureRmVM cmdlet som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="57fff-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="57fff-115">En ändring i cacheläge gör att den virtuella datorn startas om.</span><span class="sxs-lookup"><span data-stu-id="57fff-115">A change to the caching mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="57fff-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57fff-116">PARAMETERS</span></span>

### <span data-ttu-id="57fff-117">-Cachning</span><span class="sxs-lookup"><span data-stu-id="57fff-117">-Caching</span></span>
<span data-ttu-id="57fff-118">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="57fff-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="57fff-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="57fff-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57fff-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="57fff-120">ReadOnly</span></span>
- <span data-ttu-id="57fff-121">Läs</span><span class="sxs-lookup"><span data-stu-id="57fff-121">ReadWrite</span></span>

<span data-ttu-id="57fff-122">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="57fff-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="57fff-123">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="57fff-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="57fff-124">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="57fff-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fff-125">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="57fff-125">-DiskSizeInGB</span></span>
<span data-ttu-id="57fff-126">Anger storleken i GB för data disken.</span><span class="sxs-lookup"><span data-stu-id="57fff-126">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fff-127">-LUN</span><span class="sxs-lookup"><span data-stu-id="57fff-127">-Lun</span></span>
<span data-ttu-id="57fff-128">Anger LUN (Logical Unit Number) för data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="57fff-128">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fff-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="57fff-129">-Name</span></span>
<span data-ttu-id="57fff-130">Anger namnet på data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="57fff-130">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fff-131">-VM</span><span class="sxs-lookup"><span data-stu-id="57fff-131">-VM</span></span>
<span data-ttu-id="57fff-132">Anger den virtuella dator för vilken denna cmdlet ändrar en data disk.</span><span class="sxs-lookup"><span data-stu-id="57fff-132">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="57fff-133">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="57fff-133">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57fff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fff-134">CommonParameters</span></span>
<span data-ttu-id="57fff-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57fff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fff-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57fff-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fff-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57fff-137">INPUTS</span></span>

### <span data-ttu-id="57fff-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="57fff-138">None</span></span>
<span data-ttu-id="57fff-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="57fff-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57fff-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57fff-140">OUTPUTS</span></span>

## <span data-ttu-id="57fff-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57fff-141">NOTES</span></span>

## <span data-ttu-id="57fff-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57fff-142">RELATED LINKS</span></span>

[<span data-ttu-id="57fff-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="57fff-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="57fff-144">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="57fff-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


