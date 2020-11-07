---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 4ed0abb355bf7a755e5acaa36f8bb11e88d80c5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755856"
---
# <span data-ttu-id="0238b-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0238b-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="0238b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0238b-102">SYNOPSIS</span></span>
<span data-ttu-id="0238b-103">Ändrar egenskaper för en data disk för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0238b-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0238b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0238b-104">SYNTAX</span></span>

### <span data-ttu-id="0238b-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="0238b-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0238b-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="0238b-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0238b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0238b-107">DESCRIPTION</span></span>
<span data-ttu-id="0238b-108">Cmdleten **set-AzureRmVMDataDisk** ändrar egenskaper för en virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="0238b-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="0238b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0238b-109">EXAMPLES</span></span>

### <span data-ttu-id="0238b-110">Exempel 1: ändra cacheläge för en data disk</span><span class="sxs-lookup"><span data-stu-id="0238b-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="0238b-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="0238b-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="0238b-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="0238b-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="0238b-113">Det andra kommandot ändrar cacheläge för data disken med namnet DataDisk01 på den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="0238b-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="0238b-114">Kommandot skickar resultatet till Update-AzureRmVM cmdlet som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="0238b-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="0238b-115">En ändring av likviditets läget gör att den virtuella datorn startas om.</span><span class="sxs-lookup"><span data-stu-id="0238b-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="0238b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0238b-116">PARAMETERS</span></span>

### <span data-ttu-id="0238b-117">-Cachning</span><span class="sxs-lookup"><span data-stu-id="0238b-117">-Caching</span></span>
<span data-ttu-id="0238b-118">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="0238b-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="0238b-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0238b-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0238b-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0238b-120">ReadOnly</span></span>
- <span data-ttu-id="0238b-121">ReadWrite standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="0238b-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="0238b-122">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="0238b-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="0238b-123">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="0238b-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0238b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0238b-124">-DefaultProfile</span></span>
<span data-ttu-id="0238b-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0238b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0238b-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0238b-126">-DiskSizeInGB</span></span>
<span data-ttu-id="0238b-127">Anger storleken i GB för data disken.</span><span class="sxs-lookup"><span data-stu-id="0238b-127">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0238b-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="0238b-128">-Lun</span></span>
<span data-ttu-id="0238b-129">Anger LUN (Logical Unit Number) för data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0238b-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0238b-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="0238b-130">-Name</span></span>
<span data-ttu-id="0238b-131">Anger namnet på data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0238b-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0238b-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0238b-132">-StorageAccountType</span></span>
<span data-ttu-id="0238b-133">Den virtuella datorns kontotyp.</span><span class="sxs-lookup"><span data-stu-id="0238b-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0238b-134">-VM</span><span class="sxs-lookup"><span data-stu-id="0238b-134">-VM</span></span>
<span data-ttu-id="0238b-135">Anger den virtuella dator för vilken denna cmdlet ändrar en data disk.</span><span class="sxs-lookup"><span data-stu-id="0238b-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="0238b-136">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="0238b-136">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0238b-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0238b-137">-WriteAccelerator</span></span>
<span data-ttu-id="0238b-138">Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.</span><span class="sxs-lookup"><span data-stu-id="0238b-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0238b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0238b-139">CommonParameters</span></span>
<span data-ttu-id="0238b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0238b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0238b-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0238b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0238b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0238b-142">INPUTS</span></span>

### <span data-ttu-id="0238b-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0238b-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0238b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0238b-144">System.String</span></span>

### <span data-ttu-id="0238b-145">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0238b-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0238b-146">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 21.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0238b-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="0238b-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0238b-147">OUTPUTS</span></span>

### <span data-ttu-id="0238b-148">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0238b-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0238b-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0238b-149">NOTES</span></span>

## <span data-ttu-id="0238b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0238b-150">RELATED LINKS</span></span>

[<span data-ttu-id="0238b-151">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0238b-151">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0238b-152">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0238b-152">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


