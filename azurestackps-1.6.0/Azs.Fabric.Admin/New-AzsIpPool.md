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
ms.locfileid: "93571539"
---
# <span data-ttu-id="57f1b-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="57f1b-101">New-AzsIpPool</span></span>

## <span data-ttu-id="57f1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="57f1b-103">Skapa en IP-pool för infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="57f1b-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="57f1b-104">När du har skapat en IP-pool kan den inte tas bort eller ändras.</span><span class="sxs-lookup"><span data-stu-id="57f1b-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="57f1b-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57f1b-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57f1b-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57f1b-106">DESCRIPTION</span></span>
<span data-ttu-id="57f1b-107">Skapa en IP-pool för infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="57f1b-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="57f1b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57f1b-108">EXAMPLES</span></span>

### <span data-ttu-id="57f1b-109">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="57f1b-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="57f1b-110">Skapa en ny IP-pool.</span><span class="sxs-lookup"><span data-stu-id="57f1b-110">Create a new IP pool.</span></span>

## <span data-ttu-id="57f1b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57f1b-111">PARAMETERS</span></span>

### <span data-ttu-id="57f1b-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57f1b-112">-AddressPrefix</span></span>
<span data-ttu-id="57f1b-113">Adressprefixet.</span><span class="sxs-lookup"><span data-stu-id="57f1b-113">The address prefix.</span></span>

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

### <span data-ttu-id="57f1b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57f1b-114">-AsJob</span></span>
<span data-ttu-id="57f1b-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="57f1b-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="57f1b-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="57f1b-116">-EndIpAddress</span></span>
<span data-ttu-id="57f1b-117">Den sista IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="57f1b-117">The ending IP address.</span></span>

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

### <span data-ttu-id="57f1b-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="57f1b-118">-Location</span></span>
<span data-ttu-id="57f1b-119">Den region där resursen finns.</span><span class="sxs-lookup"><span data-stu-id="57f1b-119">The region where the resource is located.</span></span>

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

### <span data-ttu-id="57f1b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="57f1b-120">-Name</span></span>
<span data-ttu-id="57f1b-121">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="57f1b-121">IP pool name.</span></span>

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

### <span data-ttu-id="57f1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="57f1b-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="57f1b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="57f1b-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="57f1b-124">-StartIpAddress</span></span>
<span data-ttu-id="57f1b-125">Första IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="57f1b-125">The starting IP address.</span></span>

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

### <span data-ttu-id="57f1b-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="57f1b-126">-Tags</span></span>
<span data-ttu-id="57f1b-127">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="57f1b-127">List of key-value pairs.</span></span>

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

### <span data-ttu-id="57f1b-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57f1b-128">-Confirm</span></span>
<span data-ttu-id="57f1b-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57f1b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f1b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f1b-130">-WhatIf</span></span>
<span data-ttu-id="57f1b-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57f1b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f1b-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57f1b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f1b-133">CommonParameters</span></span>
<span data-ttu-id="57f1b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f1b-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f1b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f1b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57f1b-136">INPUTS</span></span>

## <span data-ttu-id="57f1b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57f1b-137">OUTPUTS</span></span>

### <span data-ttu-id="57f1b-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="57f1b-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="57f1b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57f1b-139">NOTES</span></span>

## <span data-ttu-id="57f1b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57f1b-140">RELATED LINKS</span></span>

