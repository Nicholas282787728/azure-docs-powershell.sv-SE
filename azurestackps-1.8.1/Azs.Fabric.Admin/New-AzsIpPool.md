---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921687"
---
# <span data-ttu-id="d40ff-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="d40ff-101">New-AzsIpPool</span></span>

## <span data-ttu-id="d40ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d40ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d40ff-103">Skapa en IP-pool för infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="d40ff-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="d40ff-104">När du har skapat en IP-pool kan den inte tas bort eller ändras.</span><span class="sxs-lookup"><span data-stu-id="d40ff-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="d40ff-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d40ff-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d40ff-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d40ff-106">DESCRIPTION</span></span>
<span data-ttu-id="d40ff-107">Skapa en IP-pool för infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="d40ff-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="d40ff-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d40ff-108">EXAMPLES</span></span>

### <span data-ttu-id="d40ff-109">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="d40ff-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="d40ff-110">Skapa en ny IP-pool.</span><span class="sxs-lookup"><span data-stu-id="d40ff-110">Create a new IP pool.</span></span>

## <span data-ttu-id="d40ff-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d40ff-111">PARAMETERS</span></span>

### <span data-ttu-id="d40ff-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="d40ff-112">-Name</span></span>
<span data-ttu-id="d40ff-113">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="d40ff-113">IP pool name.</span></span>

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

### <span data-ttu-id="d40ff-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d40ff-114">-AddressPrefix</span></span>
<span data-ttu-id="d40ff-115">Adressprefixet.</span><span class="sxs-lookup"><span data-stu-id="d40ff-115">The address prefix.</span></span>

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

### <span data-ttu-id="d40ff-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d40ff-116">-StartIpAddress</span></span>
<span data-ttu-id="d40ff-117">Första IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="d40ff-117">The starting IP address.</span></span>

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

### <span data-ttu-id="d40ff-118">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d40ff-118">-EndIpAddress</span></span>
<span data-ttu-id="d40ff-119">Den sista IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="d40ff-119">The ending IP address.</span></span>

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

### <span data-ttu-id="d40ff-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="d40ff-120">-Location</span></span>
<span data-ttu-id="d40ff-121">Den region där resursen finns.</span><span class="sxs-lookup"><span data-stu-id="d40ff-121">The region where the resource is located.</span></span>

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

### <span data-ttu-id="d40ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d40ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="d40ff-123">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="d40ff-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d40ff-124">-Taggar</span><span class="sxs-lookup"><span data-stu-id="d40ff-124">-Tags</span></span>
<span data-ttu-id="d40ff-125">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="d40ff-125">List of key-value pairs.</span></span>

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

### <span data-ttu-id="d40ff-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d40ff-126">-AsJob</span></span>
<span data-ttu-id="d40ff-127">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="d40ff-127">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d40ff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d40ff-128">-WhatIf</span></span>
<span data-ttu-id="d40ff-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d40ff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d40ff-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d40ff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d40ff-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d40ff-131">-Confirm</span></span>
<span data-ttu-id="d40ff-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d40ff-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d40ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40ff-133">CommonParameters</span></span>
<span data-ttu-id="d40ff-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d40ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40ff-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d40ff-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40ff-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d40ff-136">INPUTS</span></span>

## <span data-ttu-id="d40ff-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d40ff-137">OUTPUTS</span></span>

### <span data-ttu-id="d40ff-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="d40ff-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="d40ff-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d40ff-139">NOTES</span></span>

## <span data-ttu-id="d40ff-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d40ff-140">RELATED LINKS</span></span>
