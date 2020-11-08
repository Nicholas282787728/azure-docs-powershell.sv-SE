---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091124"
---
# <span data-ttu-id="d44f9-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d44f9-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="d44f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d44f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d44f9-103">Skapar en ny order för en enhet.</span><span class="sxs-lookup"><span data-stu-id="d44f9-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="d44f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d44f9-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d44f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d44f9-105">DESCRIPTION</span></span>
<span data-ttu-id="d44f9-106">**New-AzDataBoxEdgeOrder-** cmdleten skapar en ny order för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="d44f9-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="d44f9-107">En data Box Edge-resurs måste skapas först innan en beställning skapas.</span><span class="sxs-lookup"><span data-stu-id="d44f9-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="d44f9-108">Du kan ange information som kontakt person, företags namn, e-post, adress etc. som parametrar för att skapa beställningen.</span><span class="sxs-lookup"><span data-stu-id="d44f9-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="d44f9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d44f9-109">EXAMPLES</span></span>

### <span data-ttu-id="d44f9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d44f9-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="d44f9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d44f9-111">PARAMETERS</span></span>

### <span data-ttu-id="d44f9-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="d44f9-112">-AddressLine1</span></span>
<span data-ttu-id="d44f9-113">Adressera första raden</span><span class="sxs-lookup"><span data-stu-id="d44f9-113">Address first line</span></span>

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

### <span data-ttu-id="d44f9-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="d44f9-114">-AddressLine2</span></span>
<span data-ttu-id="d44f9-115">Adress, andra raden</span><span class="sxs-lookup"><span data-stu-id="d44f9-115">Address second line</span></span>

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

### <span data-ttu-id="d44f9-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="d44f9-116">-AddressLine3</span></span>
<span data-ttu-id="d44f9-117">Adressera tredje raden</span><span class="sxs-lookup"><span data-stu-id="d44f9-117">Address third line</span></span>

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

### <span data-ttu-id="d44f9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d44f9-118">-AsJob</span></span>
<span data-ttu-id="d44f9-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d44f9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d44f9-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="d44f9-120">-City</span></span>
<span data-ttu-id="d44f9-121">Namn på staden</span><span class="sxs-lookup"><span data-stu-id="d44f9-121">Name of the City</span></span>

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

### <span data-ttu-id="d44f9-122">-Företags namn</span><span class="sxs-lookup"><span data-stu-id="d44f9-122">-CompanyName</span></span>
<span data-ttu-id="d44f9-123">Företagets namn</span><span class="sxs-lookup"><span data-stu-id="d44f9-123">Name of the company</span></span>

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

### <span data-ttu-id="d44f9-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="d44f9-124">-ContactPerson</span></span>
<span data-ttu-id="d44f9-125">Kontakt personens namn</span><span class="sxs-lookup"><span data-stu-id="d44f9-125">Name of the contact person</span></span>

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

### <span data-ttu-id="d44f9-126">-Country</span><span class="sxs-lookup"><span data-stu-id="d44f9-126">-Country</span></span>
<span data-ttu-id="d44f9-127">Landets namn</span><span class="sxs-lookup"><span data-stu-id="d44f9-127">Name of the Country</span></span>

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

### <span data-ttu-id="d44f9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d44f9-128">-DefaultProfile</span></span>
<span data-ttu-id="d44f9-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d44f9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d44f9-130">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="d44f9-130">-DeviceName</span></span>
<span data-ttu-id="d44f9-131">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="d44f9-131">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d44f9-132">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="d44f9-132">-Email</span></span>
<span data-ttu-id="d44f9-133">Lista över e-postmeddelanden för att ta emot uppdateringar, accepterar max 10 e-postmeddelanden</span><span class="sxs-lookup"><span data-stu-id="d44f9-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="d44f9-134">-Telefon</span><span class="sxs-lookup"><span data-stu-id="d44f9-134">-Phone</span></span>
<span data-ttu-id="d44f9-135">Kontakt personens telefonnummer</span><span class="sxs-lookup"><span data-stu-id="d44f9-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="d44f9-136">-Post nummer</span><span class="sxs-lookup"><span data-stu-id="d44f9-136">-PostalCode</span></span>
<span data-ttu-id="d44f9-137">Adressens post nummer</span><span class="sxs-lookup"><span data-stu-id="d44f9-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="d44f9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d44f9-138">-ResourceGroupName</span></span>
<span data-ttu-id="d44f9-139">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d44f9-139">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d44f9-140">-State</span><span class="sxs-lookup"><span data-stu-id="d44f9-140">-State</span></span>
<span data-ttu-id="d44f9-141">Namn på tillståndet</span><span class="sxs-lookup"><span data-stu-id="d44f9-141">Name of the State</span></span>

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

### <span data-ttu-id="d44f9-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d44f9-142">-Confirm</span></span>
<span data-ttu-id="d44f9-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d44f9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d44f9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d44f9-144">-WhatIf</span></span>
<span data-ttu-id="d44f9-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d44f9-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d44f9-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d44f9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d44f9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44f9-147">CommonParameters</span></span>
<span data-ttu-id="d44f9-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d44f9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44f9-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d44f9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44f9-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d44f9-150">INPUTS</span></span>

### <span data-ttu-id="d44f9-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d44f9-151">System.String</span></span>

## <span data-ttu-id="d44f9-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d44f9-152">OUTPUTS</span></span>

### <span data-ttu-id="d44f9-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d44f9-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="d44f9-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d44f9-154">NOTES</span></span>

## <span data-ttu-id="d44f9-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d44f9-155">RELATED LINKS</span></span>