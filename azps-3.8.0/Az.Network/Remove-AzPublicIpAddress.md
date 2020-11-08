---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpAddress.md
ms.openlocfilehash: 8d3c71d1cf4df9483f379d8a689597a1a10c7ce7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091730"
---
# <span data-ttu-id="a5c46-101">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5c46-101">Remove-AzPublicIpAddress</span></span>

## <span data-ttu-id="a5c46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5c46-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c46-103">Tar bort en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="a5c46-103">Removes a public IP address.</span></span>

## <span data-ttu-id="a5c46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5c46-104">SYNTAX</span></span>

```
Remove-AzPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c46-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5c46-105">DESCRIPTION</span></span>
<span data-ttu-id="a5c46-106">Cmdleten **Remove-AzPublicIpAddress** tar bort en offentlig Azure-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="a5c46-106">The **Remove-AzPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="a5c46-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5c46-107">EXAMPLES</span></span>

### <span data-ttu-id="a5c46-108">1: ta bort en offentlig IP-adressresurs</span><span class="sxs-lookup"><span data-stu-id="a5c46-108">1: Remove a public IP address resource</span></span>
```
Remove-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="a5c46-109">Det här kommandot tar bort den offentliga IP-adressresursen som heter $publicIpName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="a5c46-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="a5c46-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5c46-110">PARAMETERS</span></span>

### <span data-ttu-id="a5c46-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5c46-111">-AsJob</span></span>
<span data-ttu-id="a5c46-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a5c46-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5c46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c46-113">-DefaultProfile</span></span>
<span data-ttu-id="a5c46-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5c46-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5c46-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a5c46-115">-Force</span></span>
<span data-ttu-id="a5c46-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a5c46-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5c46-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5c46-117">-Name</span></span>
<span data-ttu-id="a5c46-118">Anger namnet på den offentliga IP-adressen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a5c46-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c46-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5c46-119">-PassThru</span></span>
<span data-ttu-id="a5c46-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a5c46-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5c46-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a5c46-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5c46-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c46-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5c46-123">Anger namnet på den resurs grupp som innehåller den offentliga IP-adressen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a5c46-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c46-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5c46-124">-Confirm</span></span>
<span data-ttu-id="a5c46-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5c46-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c46-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c46-126">-WhatIf</span></span>
<span data-ttu-id="a5c46-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5c46-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c46-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5c46-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c46-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c46-129">CommonParameters</span></span>
<span data-ttu-id="a5c46-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c46-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c46-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c46-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c46-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5c46-132">INPUTS</span></span>

### <span data-ttu-id="a5c46-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c46-133">System.String</span></span>

## <span data-ttu-id="a5c46-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5c46-134">OUTPUTS</span></span>

### <span data-ttu-id="a5c46-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5c46-135">System.Boolean</span></span>

## <span data-ttu-id="a5c46-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5c46-136">NOTES</span></span>

## <span data-ttu-id="a5c46-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5c46-137">RELATED LINKS</span></span>

[<span data-ttu-id="a5c46-138">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5c46-138">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="a5c46-139">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5c46-139">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="a5c46-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5c46-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)

