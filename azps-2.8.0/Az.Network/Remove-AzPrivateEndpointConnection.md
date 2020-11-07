---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918994"
---
# <span data-ttu-id="77540-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="77540-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="77540-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77540-102">SYNOPSIS</span></span>
<span data-ttu-id="77540-103">Tar bort en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="77540-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="77540-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77540-104">SYNTAX</span></span>

### <span data-ttu-id="77540-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="77540-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77540-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="77540-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77540-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77540-107">DESCRIPTION</span></span>
<span data-ttu-id="77540-108">Cmdleten **Remove-AzPrivateEndpointConnection** tar bort en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="77540-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="77540-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77540-109">EXAMPLES</span></span>

### <span data-ttu-id="77540-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77540-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="77540-111">Det här exemplet tar bort en privat slut punkts anslutning med namnet MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="77540-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="77540-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77540-112">PARAMETERS</span></span>

### <span data-ttu-id="77540-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77540-113">-AsJob</span></span>
<span data-ttu-id="77540-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="77540-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77540-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77540-115">-DefaultProfile</span></span>
<span data-ttu-id="77540-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77540-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77540-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="77540-117">-Description</span></span>
<span data-ttu-id="77540-118">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="77540-118">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77540-119">-Force</span><span class="sxs-lookup"><span data-stu-id="77540-119">-Force</span></span>
<span data-ttu-id="77540-120">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="77540-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="77540-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="77540-121">-Name</span></span>
<span data-ttu-id="77540-122">Namnet på den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="77540-122">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77540-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77540-123">-PassThru</span></span>
<span data-ttu-id="77540-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="77540-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="77540-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="77540-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77540-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77540-126">-ResourceGroupName</span></span>
<span data-ttu-id="77540-127">Resurs grupps namnet för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="77540-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77540-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77540-128">-ResourceId</span></span>
<span data-ttu-id="77540-129">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="77540-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77540-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="77540-130">-ServiceName</span></span>
<span data-ttu-id="77540-131">Namnet på den privata länk tjänsten som har den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="77540-131">The name of the private link service that has the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77540-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77540-132">-Confirm</span></span>
<span data-ttu-id="77540-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77540-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77540-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77540-134">-WhatIf</span></span>
<span data-ttu-id="77540-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77540-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77540-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77540-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77540-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77540-137">CommonParameters</span></span>
<span data-ttu-id="77540-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77540-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77540-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77540-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77540-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77540-140">INPUTS</span></span>

### <span data-ttu-id="77540-141">System. String</span><span class="sxs-lookup"><span data-stu-id="77540-141">System.String</span></span>

## <span data-ttu-id="77540-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77540-142">OUTPUTS</span></span>

### <span data-ttu-id="77540-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77540-143">System.Boolean</span></span>

## <span data-ttu-id="77540-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77540-144">NOTES</span></span>

## <span data-ttu-id="77540-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77540-145">RELATED LINKS</span></span>

[<span data-ttu-id="77540-146">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="77540-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
