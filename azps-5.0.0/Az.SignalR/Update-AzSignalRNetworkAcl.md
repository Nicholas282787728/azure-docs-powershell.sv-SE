---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273170"
---
# <span data-ttu-id="b6439-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="b6439-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="b6439-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6439-102">SYNOPSIS</span></span>
<span data-ttu-id="b6439-103">Uppdatera nätverks-ACL för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="b6439-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="b6439-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6439-104">SYNTAX</span></span>

### <span data-ttu-id="b6439-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b6439-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6439-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6439-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6439-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6439-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6439-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6439-108">DESCRIPTION</span></span>
<span data-ttu-id="b6439-109">Uppdatera nätverks-ACL för en signal tjänst, inklusive standard åtgärden och nätverks åtkomst kontrol listor för offentliga och privata anslutningar.</span><span class="sxs-lookup"><span data-stu-id="b6439-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="b6439-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6439-110">EXAMPLES</span></span>

### <span data-ttu-id="b6439-111">Tillåt RESTAPI, ClientConnection för det offentliga nätverket och ange att standard åtgärd ska nekas</span><span class="sxs-lookup"><span data-stu-id="b6439-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="b6439-112">Tillåt klient anslutning och server anslutning för en privat slut punkts anslutning</span><span class="sxs-lookup"><span data-stu-id="b6439-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="b6439-113">Neka klient anslutning för både offentliga och privata anslutningar till slut punkter</span><span class="sxs-lookup"><span data-stu-id="b6439-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="b6439-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6439-114">PARAMETERS</span></span>

### <span data-ttu-id="b6439-115">-Tillåt</span><span class="sxs-lookup"><span data-stu-id="b6439-115">-Allow</span></span>
<span data-ttu-id="b6439-116">Tillåtna ACL: er för nätverk</span><span class="sxs-lookup"><span data-stu-id="b6439-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6439-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6439-117">-AsJob</span></span>
<span data-ttu-id="b6439-118">Kör cmdleten i bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="b6439-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="b6439-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="b6439-119">-DefaultAction</span></span>
<span data-ttu-id="b6439-120">Standard åtgärd hos en Signalare nätverks-ACL: er, antingen tillåta eller neka.</span><span class="sxs-lookup"><span data-stu-id="b6439-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="b6439-121">Den bestämmer om neka nätverks-ACL eller Tillåt att nätverks åtkomst kontrol listor träder i kraft.</span><span class="sxs-lookup"><span data-stu-id="b6439-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="b6439-122">Om standard åtgärden är Tillåt är det bara att neka ACL-frågor.</span><span class="sxs-lookup"><span data-stu-id="b6439-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6439-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6439-123">-DefaultProfile</span></span>
<span data-ttu-id="b6439-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6439-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6439-125">-Neka</span><span class="sxs-lookup"><span data-stu-id="b6439-125">-Deny</span></span>
<span data-ttu-id="b6439-126">Nekade nätverks åtkomst kontrol listor</span><span class="sxs-lookup"><span data-stu-id="b6439-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6439-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6439-127">-InputObject</span></span>
<span data-ttu-id="b6439-128">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="b6439-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6439-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6439-129">-Name</span></span>
<span data-ttu-id="b6439-130">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="b6439-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6439-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="b6439-131">-PrivateEndpointName</span></span>
<span data-ttu-id="b6439-132">Namn på privata slut punkter som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="b6439-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6439-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="b6439-133">-PublicNetwork</span></span>
<span data-ttu-id="b6439-134">Uppdatera åtkomst kontrol listor för offentliga nätverk</span><span class="sxs-lookup"><span data-stu-id="b6439-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="b6439-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6439-135">-ResourceGroupName</span></span>
<span data-ttu-id="b6439-136">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b6439-136">The resource group name.</span></span>
<span data-ttu-id="b6439-137">Standard alternativet används om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="b6439-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6439-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6439-138">-ResourceId</span></span>
<span data-ttu-id="b6439-139">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b6439-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6439-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6439-140">-Confirm</span></span>
<span data-ttu-id="b6439-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6439-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6439-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6439-142">-WhatIf</span></span>
<span data-ttu-id="b6439-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6439-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6439-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6439-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6439-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6439-145">CommonParameters</span></span>
<span data-ttu-id="b6439-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6439-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6439-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6439-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6439-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6439-148">INPUTS</span></span>

### <span data-ttu-id="b6439-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b6439-149">System.String</span></span>

## <span data-ttu-id="b6439-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6439-150">OUTPUTS</span></span>

### <span data-ttu-id="b6439-151">Microsoft. Azure. commands. signaler. Models. PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="b6439-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="b6439-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6439-152">NOTES</span></span>

## <span data-ttu-id="b6439-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6439-153">RELATED LINKS</span></span>
