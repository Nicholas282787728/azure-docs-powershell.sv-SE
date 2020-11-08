---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260917"
---
# <span data-ttu-id="7fd16-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="7fd16-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="7fd16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fd16-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd16-103">Register-AzStackHCI skapar en Microsoft. AzureStackHCI-moln resurs som representerar det lokala klustret och registrerar det lokala klustret med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd16-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="7fd16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fd16-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="7fd16-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fd16-105">DESCRIPTION</span></span>
<span data-ttu-id="7fd16-106">Register-AzStackHCI skapar en Microsoft. AzureStackHCI-moln resurs som representerar det lokala klustret och registrerar det lokala klustret med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd16-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="7fd16-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fd16-107">EXAMPLES</span></span>

### <span data-ttu-id="7fd16-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="7fd16-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="7fd16-109">C:\PS \> register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" resultat: lyckades ResourceID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="7fd16-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="7fd16-110">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="7fd16-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="7fd16-111">C:\PS \> register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ComputerName ClusterNode1 result: lyckades ResourceID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="7fd16-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="7fd16-112">EXEMPEL 3</span><span class="sxs-lookup"><span data-stu-id="7fd16-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="7fd16-113">C:\PS \> register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -regionen West-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG result: PendingForAdminConsent ResourceID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="7fd16-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="7fd16-114">EXEMPEL 4</span><span class="sxs-lookup"><span data-stu-id="7fd16-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="7fd16-115">C:\PS \> register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-regionen West-resourceName HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken Acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential Get-Credential result: lyckades ResourceID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="7fd16-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="7fd16-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fd16-116">PARAMETERS</span></span>

### <span data-ttu-id="7fd16-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fd16-117">-SubscriptionId</span></span>
<span data-ttu-id="7fd16-118">Anger Azure-abonnemanget för att skapa resursen.</span><span class="sxs-lookup"><span data-stu-id="7fd16-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="7fd16-119">Det här är den enda obligatoriska parametern.</span><span class="sxs-lookup"><span data-stu-id="7fd16-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd16-120">-Region</span><span class="sxs-lookup"><span data-stu-id="7fd16-120">-Region</span></span>
<span data-ttu-id="7fd16-121">Anger region för att skapa resursen.</span><span class="sxs-lookup"><span data-stu-id="7fd16-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="7fd16-122">Standardvärdet är öster.</span><span class="sxs-lookup"><span data-stu-id="7fd16-122">Default is EastUS.</span></span>

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

### <span data-ttu-id="7fd16-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7fd16-123">-ResourceName</span></span>
<span data-ttu-id="7fd16-124">Anger resurs namnet på resursen som har skapats i Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd16-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="7fd16-125">Om det inte anges används det lokala kluster namnet.</span><span class="sxs-lookup"><span data-stu-id="7fd16-125">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="7fd16-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7fd16-126">-TenantId</span></span>
<span data-ttu-id="7fd16-127">Anger Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="7fd16-127">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="7fd16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd16-128">-ResourceGroupName</span></span>
<span data-ttu-id="7fd16-129">Anger namnet på Azure Resource-gruppen.</span><span class="sxs-lookup"><span data-stu-id="7fd16-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="7fd16-130">Om ej angivet \<LocalClusterName\> -RG kommer att användas som resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7fd16-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="7fd16-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="7fd16-131">-ArmAccessToken</span></span>
<span data-ttu-id="7fd16-132">Anger ARM-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="7fd16-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="7fd16-133">Om du anger detta tillsammans med GraphAccessToken och AccountId undviks Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="7fd16-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="7fd16-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="7fd16-134">-GraphAccessToken</span></span>
<span data-ttu-id="7fd16-135">Anger Graph-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="7fd16-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="7fd16-136">Om du anger detta tillsammans med ArmAccessToken och AccountId undviks Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="7fd16-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="7fd16-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="7fd16-137">-AccountId</span></span>
<span data-ttu-id="7fd16-138">Anger ARM-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="7fd16-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="7fd16-139">Genom att ange detta tillsammans med ArmAccessToken och GraphAccessToken undviker du Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="7fd16-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd16-140">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="7fd16-140">-EnvironmentName</span></span>
<span data-ttu-id="7fd16-141">Anger Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="7fd16-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="7fd16-142">Standard är AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="7fd16-142">Default is AzureCloud.</span></span>
<span data-ttu-id="7fd16-143">Giltiga värden är AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="7fd16-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd16-144">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="7fd16-144">-ComputerName</span></span>
<span data-ttu-id="7fd16-145">Anger kluster namnet eller en av klusternoderna i det lokala klustret som registreras på Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd16-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd16-146">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="7fd16-146">-Credential</span></span>
<span data-ttu-id="7fd16-147">Anger autentiseringsuppgifter för dator namnet.</span><span class="sxs-lookup"><span data-stu-id="7fd16-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="7fd16-148">Standard är den aktuella användaren som kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7fd16-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd16-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd16-149">CommonParameters</span></span>
<span data-ttu-id="7fd16-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd16-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd16-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fd16-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd16-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fd16-152">INPUTS</span></span>

## <span data-ttu-id="7fd16-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fd16-153">OUTPUTS</span></span>

### <span data-ttu-id="7fd16-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="7fd16-154">PSCustomObject.</span></span> <span data-ttu-id="7fd16-155">Returnerar följande egenskaper i PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="7fd16-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="7fd16-156">Resultat: lyckades eller misslyckades eller PendingForAdminConsent eller avbröts.</span><span class="sxs-lookup"><span data-stu-id="7fd16-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="7fd16-157">ResourceId: resurs-ID för resursen som har skapats i Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd16-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="7fd16-158">PortalResourceURL: URL för Azure Portal resurs.</span><span class="sxs-lookup"><span data-stu-id="7fd16-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="7fd16-159">PortalAADAppPermissionsURL: URL-adressen till webbplatsen för webbplatsens program behörigheter.</span><span class="sxs-lookup"><span data-stu-id="7fd16-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="7fd16-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fd16-160">NOTES</span></span>

## <span data-ttu-id="7fd16-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fd16-161">RELATED LINKS</span></span>
