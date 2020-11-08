---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260916"
---
# <span data-ttu-id="5b4b6-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="5b4b6-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="5b4b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b4b6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4b6-103">Unregister-AzStackHCI tar bort Microsoft. AzureStackHCI-moln resursen som representerar det lokala klustret och avregistrerar det lokala klustret med Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="5b4b6-104">Den registrerade informationen i klustret används för att avregistrera klustret om inga parametrar skickas.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="5b4b6-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b4b6-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b4b6-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b4b6-106">DESCRIPTION</span></span>
<span data-ttu-id="5b4b6-107">Unregister-AzStackHCI tar bort Microsoft. AzureStackHCI-moln resursen som representerar det lokala klustret och avregistrerar det lokala klustret med Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="5b4b6-108">Den registrerade informationen i klustret används för att avregistrera klustret om inga parametrar skickas.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="5b4b6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b4b6-109">EXAMPLES</span></span>

### <span data-ttu-id="5b4b6-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="5b4b6-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="5b4b6-111">C:\PS \> -AzStackHCI resultat: lyckades</span><span class="sxs-lookup"><span data-stu-id="5b4b6-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="5b4b6-112">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="5b4b6-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="5b4b6-113">C:\PS \> Unregistered-AzStackHCI-ComputerName ClusterNode1 result: lyckades</span><span class="sxs-lookup"><span data-stu-id="5b4b6-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="5b4b6-114">EXEMPEL 3</span><span class="sxs-lookup"><span data-stu-id="5b4b6-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="5b4b6-115">C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-Confirm: $false resultat: lyckades</span><span class="sxs-lookup"><span data-stu-id="5b4b6-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="5b4b6-116">EXEMPEL 4</span><span class="sxs-lookup"><span data-stu-id="5b4b6-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="5b4b6-117">C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-resourceName HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken Acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential Get-Credential result: lyckades</span><span class="sxs-lookup"><span data-stu-id="5b4b6-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="5b4b6-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b4b6-118">PARAMETERS</span></span>

### <span data-ttu-id="5b4b6-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b4b6-119">-SubscriptionId</span></span>
<span data-ttu-id="5b4b6-120">Anger Azure-abonnemanget för att skapa resursen</span><span class="sxs-lookup"><span data-stu-id="5b4b6-120">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="5b4b6-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5b4b6-121">-ResourceName</span></span>
<span data-ttu-id="5b4b6-122">Anger resurs namnet på resursen som har skapats i Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-122">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="5b4b6-123">Om det inte anges används det lokala kluster namnet.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-123">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="5b4b6-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="5b4b6-124">-TenantId</span></span>
<span data-ttu-id="5b4b6-125">Anger Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-125">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="5b4b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b4b6-127">Anger namnet på Azure Resource-gruppen.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-127">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="5b4b6-128">Om ej angivet \<LocalClusterName\> -RG kommer att användas som resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-128">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="5b4b6-129">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="5b4b6-129">-ArmAccessToken</span></span>
<span data-ttu-id="5b4b6-130">Anger ARM-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-130">Specifies the ARM access token.</span></span>
<span data-ttu-id="5b4b6-131">Om du anger detta tillsammans med GraphAccessToken och AccountId undviks Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-131">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="5b4b6-132">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="5b4b6-132">-GraphAccessToken</span></span>
<span data-ttu-id="5b4b6-133">Anger Graph-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-133">Specifies the Graph access token.</span></span>
<span data-ttu-id="5b4b6-134">Om du anger detta tillsammans med ArmAccessToken och AccountId undviks Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-134">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="5b4b6-135">-AccountId</span><span class="sxs-lookup"><span data-stu-id="5b4b6-135">-AccountId</span></span>
<span data-ttu-id="5b4b6-136">Anger ARM-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-136">Specifies the ARM access token.</span></span>
<span data-ttu-id="5b4b6-137">Genom att ange detta tillsammans med ArmAccessToken och GraphAccessToken undviker du Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-137">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4b6-138">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="5b4b6-138">-EnvironmentName</span></span>
<span data-ttu-id="5b4b6-139">Anger Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-139">Specifies the Azure Environment.</span></span>
<span data-ttu-id="5b4b6-140">Standard är AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-140">Default is AzureCloud.</span></span>
<span data-ttu-id="5b4b6-141">Giltiga värden är AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="5b4b6-141">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4b6-142">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="5b4b6-142">-ComputerName</span></span>
<span data-ttu-id="5b4b6-143">Anger en av klusternoderna i det lokala klustret som registreras på Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-143">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4b6-144">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="5b4b6-144">-Credential</span></span>
<span data-ttu-id="5b4b6-145">Anger autentiseringsuppgifter för dator namnet.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-145">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="5b4b6-146">Standard är den aktuella användaren som kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-146">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4b6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4b6-147">-WhatIf</span></span>
<span data-ttu-id="5b4b6-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b4b6-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b4b6-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5b4b6-150">-Confirm</span></span>
<span data-ttu-id="5b4b6-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b4b6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4b6-152">CommonParameters</span></span>
<span data-ttu-id="5b4b6-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4b6-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b4b6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4b6-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b4b6-155">INPUTS</span></span>

## <span data-ttu-id="5b4b6-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b4b6-156">OUTPUTS</span></span>

### <span data-ttu-id="5b4b6-157">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-157">PSCustomObject.</span></span> <span data-ttu-id="5b4b6-158">Returnerar följande egenskaper i PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="5b4b6-158">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="5b4b6-159">Resultat: lyckades eller misslyckades eller avbröts.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-159">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="5b4b6-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b4b6-160">NOTES</span></span>

## <span data-ttu-id="5b4b6-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b4b6-161">RELATED LINKS</span></span>
