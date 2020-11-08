---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 2361fc663efc3ec4a967c718abd778599ca5340b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092365"
---
# <span data-ttu-id="8dea0-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8dea0-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="8dea0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8dea0-102">SYNOPSIS</span></span>
<span data-ttu-id="8dea0-103">Ändrar egenskaper för en data disk för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8dea0-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="8dea0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8dea0-104">SYNTAX</span></span>

### <span data-ttu-id="8dea0-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="8dea0-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dea0-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="8dea0-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dea0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8dea0-107">DESCRIPTION</span></span>
<span data-ttu-id="8dea0-108">Cmdleten **set-AzVMDataDisk** ändrar egenskaper för en virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="8dea0-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="8dea0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8dea0-109">EXAMPLES</span></span>

### <span data-ttu-id="8dea0-110">Exempel 1: ändra cacheläge för en data disk</span><span class="sxs-lookup"><span data-stu-id="8dea0-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="8dea0-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="8dea0-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="8dea0-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="8dea0-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="8dea0-113">Det andra kommandot ändrar cacheläge för data disken med namnet DataDisk01 på den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="8dea0-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="8dea0-114">Kommandot skickar resultatet till Update-AzVM cmdlet som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="8dea0-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="8dea0-115">En ändring av likviditets läget gör att den virtuella datorn startas om.</span><span class="sxs-lookup"><span data-stu-id="8dea0-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="8dea0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8dea0-116">PARAMETERS</span></span>

### <span data-ttu-id="8dea0-117">-Cachning</span><span class="sxs-lookup"><span data-stu-id="8dea0-117">-Caching</span></span>
<span data-ttu-id="8dea0-118">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="8dea0-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="8dea0-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8dea0-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8dea0-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8dea0-120">ReadOnly</span></span>
- <span data-ttu-id="8dea0-121">ReadWrite standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="8dea0-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="8dea0-122">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="8dea0-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="8dea0-123">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="8dea0-123">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="8dea0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dea0-124">-DefaultProfile</span></span>
<span data-ttu-id="8dea0-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8dea0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dea0-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8dea0-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8dea0-127">Anger resurs-ID för kund hanterad disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="8dea0-127">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="8dea0-128">Detta kan endast anges för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="8dea0-128">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="8dea0-129">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8dea0-129">-DiskSizeInGB</span></span>
<span data-ttu-id="8dea0-130">Anger storleken i GB för data disken.</span><span class="sxs-lookup"><span data-stu-id="8dea0-130">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="8dea0-131">-LUN</span><span class="sxs-lookup"><span data-stu-id="8dea0-131">-Lun</span></span>
<span data-ttu-id="8dea0-132">Anger LUN (Logical Unit Number) för data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="8dea0-132">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8dea0-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="8dea0-133">-Name</span></span>
<span data-ttu-id="8dea0-134">Anger namnet på data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="8dea0-134">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8dea0-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8dea0-135">-StorageAccountType</span></span>
<span data-ttu-id="8dea0-136">Den virtuella datorns kontotyp.</span><span class="sxs-lookup"><span data-stu-id="8dea0-136">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="8dea0-137">-VM</span><span class="sxs-lookup"><span data-stu-id="8dea0-137">-VM</span></span>
<span data-ttu-id="8dea0-138">Anger den virtuella dator för vilken denna cmdlet ändrar en data disk.</span><span class="sxs-lookup"><span data-stu-id="8dea0-138">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="8dea0-139">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="8dea0-139">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="8dea0-140">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8dea0-140">-WriteAccelerator</span></span>
<span data-ttu-id="8dea0-141">Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.</span><span class="sxs-lookup"><span data-stu-id="8dea0-141">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="8dea0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dea0-142">CommonParameters</span></span>
<span data-ttu-id="8dea0-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dea0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dea0-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dea0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dea0-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8dea0-145">INPUTS</span></span>

### <span data-ttu-id="8dea0-146">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8dea0-146">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="8dea0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8dea0-147">System.String</span></span>

### <span data-ttu-id="8dea0-148">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8dea0-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8dea0-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8dea0-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8dea0-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8dea0-150">OUTPUTS</span></span>

### <span data-ttu-id="8dea0-151">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8dea0-151">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8dea0-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8dea0-152">NOTES</span></span>

## <span data-ttu-id="8dea0-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8dea0-153">RELATED LINKS</span></span>

[<span data-ttu-id="8dea0-154">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8dea0-154">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8dea0-155">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8dea0-155">Update-AzVM</span></span>](./Update-AzVM.md)


