---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: b927e9b61e4d76795e35f2356b900b959a94e082
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924801"
---
# <span data-ttu-id="d2adf-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d2adf-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="d2adf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2adf-102">SYNOPSIS</span></span>
<span data-ttu-id="d2adf-103">Ändrar egenskaper för en data disk för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d2adf-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="d2adf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2adf-104">SYNTAX</span></span>

### <span data-ttu-id="d2adf-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="d2adf-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2adf-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="d2adf-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2adf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2adf-107">DESCRIPTION</span></span>
<span data-ttu-id="d2adf-108">Cmdleten **set-AzVMDataDisk** ändrar egenskaper för en virtuell dator data disk.</span><span class="sxs-lookup"><span data-stu-id="d2adf-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="d2adf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2adf-109">EXAMPLES</span></span>

### <span data-ttu-id="d2adf-110">Exempel 1: ändra cacheläge för en data disk</span><span class="sxs-lookup"><span data-stu-id="d2adf-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="d2adf-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="d2adf-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="d2adf-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="d2adf-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="d2adf-113">Det andra kommandot ändrar cacheläge för data disken med namnet DataDisk01 på den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="d2adf-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="d2adf-114">Kommandot skickar resultatet till Update-AzVM cmdlet som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="d2adf-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="d2adf-115">En ändring av likviditets läget gör att den virtuella datorn startas om.</span><span class="sxs-lookup"><span data-stu-id="d2adf-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="d2adf-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2adf-116">PARAMETERS</span></span>

### <span data-ttu-id="d2adf-117">-Cachning</span><span class="sxs-lookup"><span data-stu-id="d2adf-117">-Caching</span></span>
<span data-ttu-id="d2adf-118">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="d2adf-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="d2adf-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d2adf-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2adf-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d2adf-120">ReadOnly</span></span>
- <span data-ttu-id="d2adf-121">Läs</span><span class="sxs-lookup"><span data-stu-id="d2adf-121">ReadWrite</span></span>

<span data-ttu-id="d2adf-122">Standardvärdet är ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="d2adf-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="d2adf-123">Om du ändrar det här värdet startas den virtuella datorn om.</span><span class="sxs-lookup"><span data-stu-id="d2adf-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="d2adf-124">Den här inställningen påverkar diskens konsekvens och prestanda.</span><span class="sxs-lookup"><span data-stu-id="d2adf-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="d2adf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2adf-125">-DefaultProfile</span></span>
<span data-ttu-id="d2adf-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2adf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2adf-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d2adf-127">-DiskSizeInGB</span></span>
<span data-ttu-id="d2adf-128">Anger storleken i GB för data disken.</span><span class="sxs-lookup"><span data-stu-id="d2adf-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="d2adf-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="d2adf-129">-Lun</span></span>
<span data-ttu-id="d2adf-130">Anger LUN (Logical Unit Number) för data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d2adf-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d2adf-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2adf-131">-Name</span></span>
<span data-ttu-id="d2adf-132">Anger namnet på data disken som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d2adf-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d2adf-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d2adf-133">-StorageAccountType</span></span>
<span data-ttu-id="d2adf-134">Den virtuella datorns kontotyp.</span><span class="sxs-lookup"><span data-stu-id="d2adf-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="d2adf-135">-VM</span><span class="sxs-lookup"><span data-stu-id="d2adf-135">-VM</span></span>
<span data-ttu-id="d2adf-136">Anger den virtuella dator för vilken denna cmdlet ändrar en data disk.</span><span class="sxs-lookup"><span data-stu-id="d2adf-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="d2adf-137">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="d2adf-137">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="d2adf-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d2adf-138">-WriteAccelerator</span></span>
<span data-ttu-id="d2adf-139">Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.</span><span class="sxs-lookup"><span data-stu-id="d2adf-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="d2adf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2adf-140">CommonParameters</span></span>
<span data-ttu-id="d2adf-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2adf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2adf-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2adf-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2adf-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2adf-143">INPUTS</span></span>

### <span data-ttu-id="d2adf-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d2adf-144">PSVirtualMachine</span></span>
<span data-ttu-id="d2adf-145">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d2adf-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d2adf-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2adf-146">OUTPUTS</span></span>

### <span data-ttu-id="d2adf-147">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d2adf-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d2adf-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2adf-148">NOTES</span></span>

## <span data-ttu-id="d2adf-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2adf-149">RELATED LINKS</span></span>

[<span data-ttu-id="d2adf-150">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2adf-150">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d2adf-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2adf-151">Update-AzVM</span></span>](./Update-AzVM.md)


