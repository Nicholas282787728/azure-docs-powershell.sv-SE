---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: c88365a64c9102b74811fedb2d93e103346e5a50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744827"
---
# <span data-ttu-id="d0a1e-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="d0a1e-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="d0a1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a1e-103">Skapar ett nytt data-jobb med de angivna parametrarna</span><span class="sxs-lookup"><span data-stu-id="d0a1e-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="d0a1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0a1e-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0a1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0a1e-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a1e-106">**New-AzDataBoxJob-** cmdleten används för att skapa ett nytt data-jobb genom att ange den information som krävs för att skapa jobbet.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="d0a1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0a1e-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a1e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0a1e-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="d0a1e-109">Cmdleten tar alla nödvändiga parametrar och vissa valfria parametrar för att skapa data bladet.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="d0a1e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0a1e-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a1e-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="d0a1e-111">-AddressType</span></span>
<span data-ttu-id="d0a1e-112">Typ av adress.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-112">Type of Address.</span></span> <span data-ttu-id="d0a1e-113">Tillgängliga värden: AddressType. None (standard), AddressType. boende, AddressType. Commercial</span><span class="sxs-lookup"><span data-stu-id="d0a1e-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-114">-Ort</span><span class="sxs-lookup"><span data-stu-id="d0a1e-114">-City</span></span>
<span data-ttu-id="d0a1e-115">Namn på staden.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-115">Name of the City.</span></span> <span data-ttu-id="d0a1e-116">Ex: San Francisco</span><span class="sxs-lookup"><span data-stu-id="d0a1e-116">Ex : San Francisco</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-117">-Företags namn</span><span class="sxs-lookup"><span data-stu-id="d0a1e-117">-CompanyName</span></span>
<span data-ttu-id="d0a1e-118">Företagets namn</span><span class="sxs-lookup"><span data-stu-id="d0a1e-118">Name of the company</span></span>

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

### <span data-ttu-id="d0a1e-119">-Kontakt namn</span><span class="sxs-lookup"><span data-stu-id="d0a1e-119">-ContactName</span></span>
<span data-ttu-id="d0a1e-120">Kontakt namn</span><span class="sxs-lookup"><span data-stu-id="d0a1e-120">Contact Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="d0a1e-121">-CountryCode</span></span>
<span data-ttu-id="d0a1e-122">Landskod.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-122">Country Code.</span></span> <span data-ttu-id="d0a1e-123">Ex: USA</span><span class="sxs-lookup"><span data-stu-id="d0a1e-123">Ex: US</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="d0a1e-124">-DataBoxType</span></span>
<span data-ttu-id="d0a1e-125">Data typen SKU.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-125">Sku type of Databox.</span></span>  <span data-ttu-id="d0a1e-126">Tillgängliga värden: DataBoxDisk, dataDataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="d0a1e-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a1e-127">-DefaultProfile</span></span>
<span data-ttu-id="d0a1e-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a1e-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="d0a1e-129">-EmailId</span></span>
<span data-ttu-id="d0a1e-130">Lista med EmailIds kan tillhandahållas.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="d0a1e-131">Minst ett är obligatoriskt</span><span class="sxs-lookup"><span data-stu-id="d0a1e-131">Atleast one is mandatory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="d0a1e-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="d0a1e-133">För DataBoxDisk order är det obligatoriskt att ange förväntat data i terabyte.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="d0a1e-134">-Location</span></span>
<span data-ttu-id="d0a1e-135">Prenumerationens plats</span><span class="sxs-lookup"><span data-stu-id="d0a1e-135">Location of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0a1e-136">-Name</span></span>
<span data-ttu-id="d0a1e-137">Namnet på det data rutan som ska skapas</span><span class="sxs-lookup"><span data-stu-id="d0a1e-137">Name of the databox job to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-138">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="d0a1e-138">-PhoneNumber</span></span>
<span data-ttu-id="d0a1e-139">Kontakt nummer</span><span class="sxs-lookup"><span data-stu-id="d0a1e-139">Contact Number</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-140">-Post nummer</span><span class="sxs-lookup"><span data-stu-id="d0a1e-140">-PostalCode</span></span>
<span data-ttu-id="d0a1e-141">Post nummer</span><span class="sxs-lookup"><span data-stu-id="d0a1e-141">Postal Code</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a1e-142">-ResourceGroupName</span></span>
<span data-ttu-id="d0a1e-143">Resurs grupps namn som du vill skapa ett data i.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-143">Resource Group Name under which the databox job has to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="d0a1e-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="d0a1e-145">Ange delstat eller landskod.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-145">Input the state or province code.</span></span> <span data-ttu-id="d0a1e-146">Gilla CA – California; FL-Florida; NY-New York</span><span class="sxs-lookup"><span data-stu-id="d0a1e-146">Like CA - California; FL - Florida; NY - New York</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d0a1e-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="d0a1e-148">Lista över resurs-ID: n för lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="d0a1e-149">Minst ett är obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="d0a1e-150">-StreetAddress1</span></span>
<span data-ttu-id="d0a1e-151">Gatuadress</span><span class="sxs-lookup"><span data-stu-id="d0a1e-151">Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="d0a1e-152">-StreetAddress2</span></span>
<span data-ttu-id="d0a1e-153">Ytterligare gatuadress</span><span class="sxs-lookup"><span data-stu-id="d0a1e-153">Additional Street Address</span></span>

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

### <span data-ttu-id="d0a1e-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="d0a1e-154">-StreetAddress3</span></span>
<span data-ttu-id="d0a1e-155">Ytterligare gatuadress</span><span class="sxs-lookup"><span data-stu-id="d0a1e-155">Additional Street Address</span></span>

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

### <span data-ttu-id="d0a1e-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0a1e-156">-Confirm</span></span>
<span data-ttu-id="d0a1e-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a1e-158">-WhatIf</span></span>
<span data-ttu-id="d0a1e-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0a1e-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a1e-161">CommonParameters</span></span>
<span data-ttu-id="d0a1e-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a1e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a1e-163">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0a1e-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a1e-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0a1e-164">INPUTS</span></span>

### <span data-ttu-id="d0a1e-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="d0a1e-165">System.String[]</span></span>

## <span data-ttu-id="d0a1e-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0a1e-166">OUTPUTS</span></span>

### <span data-ttu-id="d0a1e-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="d0a1e-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="d0a1e-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0a1e-168">NOTES</span></span>

## <span data-ttu-id="d0a1e-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0a1e-169">RELATED LINKS</span></span>
