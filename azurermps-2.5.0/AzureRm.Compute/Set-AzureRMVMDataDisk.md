---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: 53ad88f6e3df11eb3a8f2f9c4b21af40b9ea614b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931481"
---
# <span data-ttu-id="0e785-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0e785-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="0e785-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e785-102">SYNOPSIS</span></span>
<span data-ttu-id="0e785-103">Ändrar egenskaper för en data disk för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0e785-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e785-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e785-104">SYNTAX</span></span>

### <span data-ttu-id="0e785-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="0e785-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e785-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="0e785-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e785-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e785-107">DESCRIPTION</span></span>
<span data-ttu-id="0e785-108">Cmdleten **set-AzureRmVMDataDisk** ändrar egenskaper för en virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="0e785-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="0e785-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e785-109">EXAMPLES</span></span>

### <span data-ttu-id="0e785-110">Exempel 1: ändra cacheläge för en data disk</span><span class="sxs-lookup"><span data-stu-id="0e785-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="0e785-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="0e785-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="0e785-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="0e785-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="0e785-113">Det andra kommandot ändrar cacheläge för data disken med namnet DataDisk01 på den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="0e785-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="0e785-114">Kommandot skickar resultatet till Update-AzureRmVM cmdlet som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="0e785-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="0e785-115">En ändring av likviditets läget gör att den virtuella datorn startas om.</span><span class="sxs-lookup"><span data-stu-id="0e785-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="0e785-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e785-116">PARAMETERS</span></span>

### <span data-ttu-id="0e785-117">-Cachning</span><span class="sxs-lookup"><span data-stu-id="0e785-117">-Caching</span></span>
<span data-ttu-id="0e785-118">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="0e785-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="0e785-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0e785-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e785-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0e785-120">ReadOnly</span></span>
- <span data-ttu-id="0e785-121">Läs</span><span class="sxs-lookup"><span data-stu-id="0e785-121">ReadWrite</span></span>

<span data-ttu-id="0e785-122">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="0e785-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="0e785-123">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="0e785-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="0e785-124">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="0e785-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="0e785-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e785-125">-DefaultProfile</span></span>
<span data-ttu-id="0e785-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e785-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e785-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0e785-127">-DiskSizeInGB</span></span>
<span data-ttu-id="0e785-128">Anger storleken i GB för data disken.</span><span class="sxs-lookup"><span data-stu-id="0e785-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="0e785-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="0e785-129">-Lun</span></span>
<span data-ttu-id="0e785-130">Anger LUN (Logical Unit Number) för data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0e785-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0e785-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e785-131">-Name</span></span>
<span data-ttu-id="0e785-132">Anger namnet på data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0e785-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0e785-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0e785-133">-StorageAccountType</span></span>
<span data-ttu-id="0e785-134">Den virtuella datorns kontotyp.</span><span class="sxs-lookup"><span data-stu-id="0e785-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e785-135">-VM</span><span class="sxs-lookup"><span data-stu-id="0e785-135">-VM</span></span>
<span data-ttu-id="0e785-136">Anger den virtuella dator för vilken denna cmdlet ändrar en data disk.</span><span class="sxs-lookup"><span data-stu-id="0e785-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="0e785-137">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="0e785-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="0e785-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0e785-138">-WriteAccelerator</span></span>
<span data-ttu-id="0e785-139">Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.</span><span class="sxs-lookup"><span data-stu-id="0e785-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e785-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e785-140">CommonParameters</span></span>
<span data-ttu-id="0e785-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e785-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e785-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e785-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e785-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e785-143">INPUTS</span></span>

### <span data-ttu-id="0e785-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0e785-144">PSVirtualMachine</span></span>
<span data-ttu-id="0e785-145">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0e785-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="0e785-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e785-146">OUTPUTS</span></span>

### <span data-ttu-id="0e785-147">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0e785-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0e785-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e785-148">NOTES</span></span>

## <span data-ttu-id="0e785-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e785-149">RELATED LINKS</span></span>

[<span data-ttu-id="0e785-150">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0e785-150">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0e785-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0e785-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


