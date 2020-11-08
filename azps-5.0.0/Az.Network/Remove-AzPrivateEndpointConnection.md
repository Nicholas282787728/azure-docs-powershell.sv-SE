---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271336"
---
# <span data-ttu-id="640a4-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="640a4-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="640a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="640a4-102">SYNOPSIS</span></span>
<span data-ttu-id="640a4-103">Tar bort en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="640a4-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="640a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="640a4-104">SYNTAX</span></span>

### <span data-ttu-id="640a4-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="640a4-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="640a4-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="640a4-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="640a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="640a4-107">DESCRIPTION</span></span>
<span data-ttu-id="640a4-108">Cmdleten **Remove-AzPrivateEndpointConnection** tar bort en privat slut punkts anslutning.</span><span class="sxs-lookup"><span data-stu-id="640a4-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="640a4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="640a4-109">EXAMPLES</span></span>

### <span data-ttu-id="640a4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="640a4-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="640a4-111">Det här exemplet tar bort en privat slut punkts anslutning med namnet MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="640a4-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="640a4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="640a4-112">PARAMETERS</span></span>

### <span data-ttu-id="640a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="640a4-113">-AsJob</span></span>
<span data-ttu-id="640a4-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="640a4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="640a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640a4-115">-DefaultProfile</span></span>
<span data-ttu-id="640a4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="640a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="640a4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="640a4-117">-Force</span></span>
<span data-ttu-id="640a4-118">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="640a4-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="640a4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="640a4-119">-Name</span></span>
<span data-ttu-id="640a4-120">Namnet på den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="640a4-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="640a4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="640a4-121">-PassThru</span></span>
<span data-ttu-id="640a4-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="640a4-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="640a4-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="640a4-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="640a4-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="640a4-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="640a4-125">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="640a4-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640a4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640a4-126">-ResourceGroupName</span></span>
<span data-ttu-id="640a4-127">Resurs grupps namnet för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="640a4-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="640a4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="640a4-128">-ResourceId</span></span>
<span data-ttu-id="640a4-129">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="640a4-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="640a4-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="640a4-130">-ServiceName</span></span>
<span data-ttu-id="640a4-131">Namnet på den tjänst som den privata slut punkts anslutningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="640a4-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="640a4-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="640a4-132">-Confirm</span></span>
<span data-ttu-id="640a4-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="640a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="640a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="640a4-134">-WhatIf</span></span>
<span data-ttu-id="640a4-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="640a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="640a4-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="640a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="640a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640a4-137">CommonParameters</span></span>
<span data-ttu-id="640a4-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640a4-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="640a4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640a4-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="640a4-140">INPUTS</span></span>

### <span data-ttu-id="640a4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="640a4-141">System.String</span></span>

## <span data-ttu-id="640a4-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="640a4-142">OUTPUTS</span></span>

### <span data-ttu-id="640a4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="640a4-143">System.Boolean</span></span>

## <span data-ttu-id="640a4-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="640a4-144">NOTES</span></span>

## <span data-ttu-id="640a4-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="640a4-145">RELATED LINKS</span></span>

[<span data-ttu-id="640a4-146">Godkänn-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="640a4-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="640a4-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="640a4-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="640a4-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="640a4-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="640a4-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="640a4-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
