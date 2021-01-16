---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418888"
---
# <span data-ttu-id="93b8e-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="93b8e-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="93b8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="93b8e-103">Unregister-AzStackHCI tar bort Microsoft. AzureStackHCI-moln resursen som representerar det lokala klustret och avregistrerar det lokala klustret med Azure.</span><span class="sxs-lookup"><span data-stu-id="93b8e-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="93b8e-104">Den registrerade informationen i klustret används för att avregistrera klustret om inga parametrar skickas.</span><span class="sxs-lookup"><span data-stu-id="93b8e-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="93b8e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93b8e-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93b8e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93b8e-106">DESCRIPTION</span></span>
<span data-ttu-id="93b8e-107">Unregister-AzStackHCI tar bort Microsoft. AzureStackHCI-moln resursen som representerar det lokala klustret och avregistrerar det lokala klustret med Azure.</span><span class="sxs-lookup"><span data-stu-id="93b8e-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="93b8e-108">Den registrerade informationen i klustret används för att avregistrera klustret om inga parametrar skickas.</span><span class="sxs-lookup"><span data-stu-id="93b8e-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="93b8e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93b8e-109">EXAMPLES</span></span>

### <span data-ttu-id="93b8e-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="93b8e-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="93b8e-111">C:\PS \> -AzStackHCI resultat: lyckades</span><span class="sxs-lookup"><span data-stu-id="93b8e-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="93b8e-112">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="93b8e-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="93b8e-113">C:\PS \> Unregistered-AzStackHCI-ComputerName ClusterNode1 result: lyckades</span><span class="sxs-lookup"><span data-stu-id="93b8e-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="93b8e-114">EXEMPEL 3</span><span class="sxs-lookup"><span data-stu-id="93b8e-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="93b8e-115">C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false resultat: lyckades</span><span class="sxs-lookup"><span data-stu-id="93b8e-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="93b8e-116">EXEMPEL 4</span><span class="sxs-lookup"><span data-stu-id="93b8e-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="93b8e-117">C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-resourceName HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken Acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential Get-Credential result: lyckades</span><span class="sxs-lookup"><span data-stu-id="93b8e-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="93b8e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93b8e-118">PARAMETERS</span></span>

### <span data-ttu-id="93b8e-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="93b8e-119">-AccountId</span></span>
<span data-ttu-id="93b8e-120">Anger ARM-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="93b8e-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="93b8e-121">Genom att ange detta tillsammans med ArmAccessToken och GraphAccessToken undviker du Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="93b8e-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="93b8e-122">-ArmAccessToken</span></span>
<span data-ttu-id="93b8e-123">Anger ARM-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="93b8e-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="93b8e-124">Om du anger detta tillsammans med GraphAccessToken och AccountId undviks Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="93b8e-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="93b8e-125">-ComputerName</span></span>
<span data-ttu-id="93b8e-126">Anger en av klusternoderna i det lokala klustret som registreras på Azure.</span><span class="sxs-lookup"><span data-stu-id="93b8e-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-127">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="93b8e-127">-Credential</span></span>
<span data-ttu-id="93b8e-128">Anger autentiseringsuppgifter för dator namnet.</span><span class="sxs-lookup"><span data-stu-id="93b8e-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="93b8e-129">Standard är den aktuella användaren som kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93b8e-129">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="93b8e-130">-EnvironmentName</span></span>
<span data-ttu-id="93b8e-131">Anger Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="93b8e-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="93b8e-132">Standard är AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="93b8e-132">Default is AzureCloud.</span></span>
<span data-ttu-id="93b8e-133">Giltiga värden är AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="93b8e-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="93b8e-134">-GraphAccessToken</span></span>
<span data-ttu-id="93b8e-135">Anger Graph-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="93b8e-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="93b8e-136">Om du anger detta tillsammans med ArmAccessToken och AccountId undviks Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="93b8e-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b8e-137">-ResourceGroupName</span></span>
<span data-ttu-id="93b8e-138">Anger namnet på Azure Resource-gruppen.</span><span class="sxs-lookup"><span data-stu-id="93b8e-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="93b8e-139">Om ej angivet \<LocalClusterName\> -RG kommer att användas som resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="93b8e-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="93b8e-140">-ResourceName</span></span>
<span data-ttu-id="93b8e-141">Anger resurs namnet på resursen som har skapats i Azure.</span><span class="sxs-lookup"><span data-stu-id="93b8e-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="93b8e-142">Om det inte anges används det lokala kluster namnet.</span><span class="sxs-lookup"><span data-stu-id="93b8e-142">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93b8e-143">-SubscriptionId</span></span>
<span data-ttu-id="93b8e-144">Anger Azure-abonnemanget för att skapa resursen</span><span class="sxs-lookup"><span data-stu-id="93b8e-144">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="93b8e-145">-TenantId</span></span>
<span data-ttu-id="93b8e-146">Anger Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="93b8e-146">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="93b8e-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="93b8e-148">Använd enhets kod i stället för en interaktiv webbläsare.</span><span class="sxs-lookup"><span data-stu-id="93b8e-148">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b8e-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93b8e-149">-Confirm</span></span>
<span data-ttu-id="93b8e-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93b8e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93b8e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93b8e-151">-WhatIf</span></span>
<span data-ttu-id="93b8e-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93b8e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93b8e-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93b8e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93b8e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b8e-154">CommonParameters</span></span>
<span data-ttu-id="93b8e-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b8e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b8e-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93b8e-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b8e-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93b8e-157">INPUTS</span></span>

## <span data-ttu-id="93b8e-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93b8e-158">OUTPUTS</span></span>

### <span data-ttu-id="93b8e-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="93b8e-159">PSCustomObject.</span></span> <span data-ttu-id="93b8e-160">Returnerar följande egenskaper i PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="93b8e-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="93b8e-161">Resultat: lyckades eller misslyckades eller avbröts.</span><span class="sxs-lookup"><span data-stu-id="93b8e-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="93b8e-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93b8e-162">NOTES</span></span>

## <span data-ttu-id="93b8e-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93b8e-163">RELATED LINKS</span></span>
