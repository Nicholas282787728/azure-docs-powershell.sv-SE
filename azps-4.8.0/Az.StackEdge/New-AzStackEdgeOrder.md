---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260943"
---
# <span data-ttu-id="191eb-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="191eb-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="191eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="191eb-102">SYNOPSIS</span></span>
<span data-ttu-id="191eb-103">Skapar en ny order för en enhet.</span><span class="sxs-lookup"><span data-stu-id="191eb-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="191eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="191eb-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="191eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="191eb-105">DESCRIPTION</span></span>
<span data-ttu-id="191eb-106">Cmdleten **New-AzStackEdgeOrder** skapar en ny order för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="191eb-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="191eb-107">Du måste först skapa en enhets resurs för att skapa en beställning.</span><span class="sxs-lookup"><span data-stu-id="191eb-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="191eb-108">Du kan ange information som kontakt person, företags namn, e-post, adress etc. som parametrar för att skapa beställningen.</span><span class="sxs-lookup"><span data-stu-id="191eb-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="191eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="191eb-109">EXAMPLES</span></span>

### <span data-ttu-id="191eb-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="191eb-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="191eb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="191eb-111">PARAMETERS</span></span>

### <span data-ttu-id="191eb-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="191eb-112">-AddressLine1</span></span>
<span data-ttu-id="191eb-113">Adressera första raden</span><span class="sxs-lookup"><span data-stu-id="191eb-113">Address first line</span></span>

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

### <span data-ttu-id="191eb-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="191eb-114">-AddressLine2</span></span>
<span data-ttu-id="191eb-115">Adress, andra raden</span><span class="sxs-lookup"><span data-stu-id="191eb-115">Address second line</span></span>

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

### <span data-ttu-id="191eb-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="191eb-116">-AddressLine3</span></span>
<span data-ttu-id="191eb-117">Adressera tredje raden</span><span class="sxs-lookup"><span data-stu-id="191eb-117">Address third line</span></span>

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

### <span data-ttu-id="191eb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="191eb-118">-AsJob</span></span>
<span data-ttu-id="191eb-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="191eb-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="191eb-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="191eb-120">-City</span></span>
<span data-ttu-id="191eb-121">Namn på staden</span><span class="sxs-lookup"><span data-stu-id="191eb-121">Name of the City</span></span>

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

### <span data-ttu-id="191eb-122">-Företags namn</span><span class="sxs-lookup"><span data-stu-id="191eb-122">-CompanyName</span></span>
<span data-ttu-id="191eb-123">Företagets namn</span><span class="sxs-lookup"><span data-stu-id="191eb-123">Name of the company</span></span>

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

### <span data-ttu-id="191eb-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="191eb-124">-ContactPerson</span></span>
<span data-ttu-id="191eb-125">Kontakt personens namn</span><span class="sxs-lookup"><span data-stu-id="191eb-125">Name of the contact person</span></span>

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

### <span data-ttu-id="191eb-126">-Country</span><span class="sxs-lookup"><span data-stu-id="191eb-126">-Country</span></span>
<span data-ttu-id="191eb-127">Landets namn</span><span class="sxs-lookup"><span data-stu-id="191eb-127">Name of the Country</span></span>

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

### <span data-ttu-id="191eb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191eb-128">-DefaultProfile</span></span>
<span data-ttu-id="191eb-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="191eb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="191eb-130">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="191eb-130">-DeviceName</span></span>
<span data-ttu-id="191eb-131">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="191eb-131">Resource Name</span></span>

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

### <span data-ttu-id="191eb-132">-E-postadress</span><span class="sxs-lookup"><span data-stu-id="191eb-132">-Email</span></span>
<span data-ttu-id="191eb-133">Lista över e-postmeddelanden för att ta emot uppdateringar, accepterar max 10 e-postmeddelanden</span><span class="sxs-lookup"><span data-stu-id="191eb-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="191eb-134">-Telefon</span><span class="sxs-lookup"><span data-stu-id="191eb-134">-Phone</span></span>
<span data-ttu-id="191eb-135">Kontakt personens telefonnummer</span><span class="sxs-lookup"><span data-stu-id="191eb-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="191eb-136">-Post nummer</span><span class="sxs-lookup"><span data-stu-id="191eb-136">-PostalCode</span></span>
<span data-ttu-id="191eb-137">Adressens post nummer</span><span class="sxs-lookup"><span data-stu-id="191eb-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="191eb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="191eb-138">-ResourceGroupName</span></span>
<span data-ttu-id="191eb-139">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="191eb-139">Resource Group Name</span></span>

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

### <span data-ttu-id="191eb-140">-State</span><span class="sxs-lookup"><span data-stu-id="191eb-140">-State</span></span>
<span data-ttu-id="191eb-141">Namn på tillståndet</span><span class="sxs-lookup"><span data-stu-id="191eb-141">Name of the State</span></span>

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

### <span data-ttu-id="191eb-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="191eb-142">-Confirm</span></span>
<span data-ttu-id="191eb-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="191eb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="191eb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="191eb-144">-WhatIf</span></span>
<span data-ttu-id="191eb-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="191eb-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="191eb-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="191eb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="191eb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191eb-147">CommonParameters</span></span>
<span data-ttu-id="191eb-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="191eb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191eb-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="191eb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191eb-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="191eb-150">INPUTS</span></span>

### <span data-ttu-id="191eb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="191eb-151">System.String</span></span>

## <span data-ttu-id="191eb-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="191eb-152">OUTPUTS</span></span>

### <span data-ttu-id="191eb-153">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="191eb-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="191eb-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="191eb-154">NOTES</span></span>

## <span data-ttu-id="191eb-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="191eb-155">RELATED LINKS</span></span>
