---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572315"
---
# <span data-ttu-id="a6f71-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="a6f71-101">New-AzsIpPool</span></span>

## <span data-ttu-id="a6f71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6f71-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f71-103">Skapa en IP-pool för infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="a6f71-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="a6f71-104">När du har skapat en IP-pool kan den inte tas bort eller ändras.</span><span class="sxs-lookup"><span data-stu-id="a6f71-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="a6f71-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6f71-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6f71-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6f71-106">DESCRIPTION</span></span>
<span data-ttu-id="a6f71-107">Skapa en IP-pool för infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="a6f71-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="a6f71-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6f71-108">EXAMPLES</span></span>

### <span data-ttu-id="a6f71-109">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6f71-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="a6f71-110">Skapa en ny IP-pool.</span><span class="sxs-lookup"><span data-stu-id="a6f71-110">Create a new IP pool.</span></span>

## <span data-ttu-id="a6f71-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6f71-111">PARAMETERS</span></span>

### <span data-ttu-id="a6f71-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a6f71-112">-AddressPrefix</span></span>
<span data-ttu-id="a6f71-113">Adressprefixet.</span><span class="sxs-lookup"><span data-stu-id="a6f71-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6f71-114">-AsJob</span></span>
<span data-ttu-id="a6f71-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="a6f71-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a6f71-116">-EndIpAddress</span></span>
<span data-ttu-id="a6f71-117">Den sista IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="a6f71-117">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="a6f71-118">-Location</span></span>
<span data-ttu-id="a6f71-119">Den region där resursen finns.</span><span class="sxs-lookup"><span data-stu-id="a6f71-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a6f71-120">-Name</span></span>
<span data-ttu-id="a6f71-121">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="a6f71-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6f71-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6f71-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="a6f71-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a6f71-124">-StartIpAddress</span></span>
<span data-ttu-id="a6f71-125">Första IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="a6f71-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="a6f71-126">-Tags</span></span>
<span data-ttu-id="a6f71-127">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a6f71-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6f71-128">-Confirm</span></span>
<span data-ttu-id="a6f71-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6f71-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6f71-130">-WhatIf</span></span>
<span data-ttu-id="a6f71-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6f71-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6f71-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6f71-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f71-133">CommonParameters</span></span>
<span data-ttu-id="a6f71-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f71-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f71-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f71-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6f71-136">INPUTS</span></span>

## <span data-ttu-id="a6f71-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6f71-137">OUTPUTS</span></span>

### <span data-ttu-id="a6f71-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="a6f71-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="a6f71-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6f71-139">NOTES</span></span>

## <span data-ttu-id="a6f71-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6f71-140">RELATED LINKS</span></span>

