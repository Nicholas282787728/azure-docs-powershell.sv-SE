---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272327"
---
# <span data-ttu-id="6a165-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a165-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="6a165-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a165-102">SYNOPSIS</span></span>
<span data-ttu-id="6a165-103">Tar bort en CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="6a165-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="6a165-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a165-104">SYNTAX</span></span>

### <span data-ttu-id="6a165-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a165-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a165-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a165-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a165-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a165-107">DESCRIPTION</span></span>
<span data-ttu-id="6a165-108">Cmdleten **Remove-AzCdnEndpoint** tar bort en slut punkt för Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="6a165-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6a165-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a165-109">EXAMPLES</span></span>

## <span data-ttu-id="6a165-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a165-110">PARAMETERS</span></span>

### <span data-ttu-id="6a165-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a165-111">-CdnEndpoint</span></span>
<span data-ttu-id="6a165-112">Anger slut punkten som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="6a165-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a165-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a165-113">-DefaultProfile</span></span>
<span data-ttu-id="6a165-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6a165-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a165-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6a165-115">-EndpointName</span></span>
<span data-ttu-id="6a165-116">Anger namnet på den slut punkt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="6a165-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a165-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6a165-117">-Force</span></span>
<span data-ttu-id="6a165-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6a165-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a165-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a165-119">-PassThru</span></span>
<span data-ttu-id="6a165-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="6a165-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a165-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="6a165-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a165-122">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="6a165-122">-ProfileName</span></span>
<span data-ttu-id="6a165-123">Anger namnet på den profil som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="6a165-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a165-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a165-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a165-125">Anger namnet på resurs gruppen som slut punkten hör till.</span><span class="sxs-lookup"><span data-stu-id="6a165-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a165-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a165-126">-Confirm</span></span>
<span data-ttu-id="6a165-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a165-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a165-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a165-128">-WhatIf</span></span>
<span data-ttu-id="6a165-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a165-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a165-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a165-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a165-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a165-131">CommonParameters</span></span>
<span data-ttu-id="6a165-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a165-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a165-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a165-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a165-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a165-134">INPUTS</span></span>

### <span data-ttu-id="6a165-135">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a165-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="6a165-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6a165-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6a165-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a165-137">OUTPUTS</span></span>

### <span data-ttu-id="6a165-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a165-138">System.Boolean</span></span>

## <span data-ttu-id="6a165-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a165-139">NOTES</span></span>

## <span data-ttu-id="6a165-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a165-140">RELATED LINKS</span></span>

[<span data-ttu-id="6a165-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a165-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="6a165-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a165-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="6a165-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a165-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="6a165-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a165-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="6a165-145">Stopp-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a165-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


