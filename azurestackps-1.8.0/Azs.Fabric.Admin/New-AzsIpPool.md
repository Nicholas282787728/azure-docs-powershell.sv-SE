---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921349"
---
# <span data-ttu-id="2ea85-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="2ea85-101">New-AzsIpPool</span></span>

## <span data-ttu-id="2ea85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ea85-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea85-103">Skapa en IP-pool för infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="2ea85-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="2ea85-104">När du har skapat en IP-pool kan den inte tas bort eller ändras.</span><span class="sxs-lookup"><span data-stu-id="2ea85-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="2ea85-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ea85-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ea85-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ea85-106">DESCRIPTION</span></span>
<span data-ttu-id="2ea85-107">Skapa en IP-pool för infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="2ea85-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="2ea85-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ea85-108">EXAMPLES</span></span>

### <span data-ttu-id="2ea85-109">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="2ea85-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="2ea85-110">Skapa en ny IP-pool.</span><span class="sxs-lookup"><span data-stu-id="2ea85-110">Create a new IP pool.</span></span>

## <span data-ttu-id="2ea85-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ea85-111">PARAMETERS</span></span>

### <span data-ttu-id="2ea85-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ea85-112">-Name</span></span>
<span data-ttu-id="2ea85-113">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="2ea85-113">IP pool name.</span></span>

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

### <span data-ttu-id="2ea85-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2ea85-114">-AddressPrefix</span></span>
<span data-ttu-id="2ea85-115">Adressprefixet.</span><span class="sxs-lookup"><span data-stu-id="2ea85-115">The address prefix.</span></span>

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

### <span data-ttu-id="2ea85-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2ea85-116">-StartIpAddress</span></span>
<span data-ttu-id="2ea85-117">Första IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="2ea85-117">The starting IP address.</span></span>

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

### <span data-ttu-id="2ea85-118">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="2ea85-118">-EndIpAddress</span></span>
<span data-ttu-id="2ea85-119">Den sista IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="2ea85-119">The ending IP address.</span></span>

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

### <span data-ttu-id="2ea85-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="2ea85-120">-Location</span></span>
<span data-ttu-id="2ea85-121">Den region där resursen finns.</span><span class="sxs-lookup"><span data-stu-id="2ea85-121">The region where the resource is located.</span></span>

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

### <span data-ttu-id="2ea85-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea85-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ea85-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="2ea85-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2ea85-124">-Taggar</span><span class="sxs-lookup"><span data-stu-id="2ea85-124">-Tags</span></span>
<span data-ttu-id="2ea85-125">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="2ea85-125">List of key-value pairs.</span></span>

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

### <span data-ttu-id="2ea85-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ea85-126">-AsJob</span></span>
<span data-ttu-id="2ea85-127">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="2ea85-127">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2ea85-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea85-128">-WhatIf</span></span>
<span data-ttu-id="2ea85-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ea85-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea85-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ea85-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea85-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ea85-131">-Confirm</span></span>
<span data-ttu-id="2ea85-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ea85-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea85-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea85-133">CommonParameters</span></span>
<span data-ttu-id="2ea85-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea85-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea85-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea85-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea85-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ea85-136">INPUTS</span></span>

## <span data-ttu-id="2ea85-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ea85-137">OUTPUTS</span></span>

### <span data-ttu-id="2ea85-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="2ea85-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="2ea85-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ea85-139">NOTES</span></span>

## <span data-ttu-id="2ea85-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ea85-140">RELATED LINKS</span></span>
