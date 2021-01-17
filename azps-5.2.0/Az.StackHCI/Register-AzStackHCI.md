---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: ad9c09118252499f99708ae99d36ee9ba2418ff2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404416"
---
# <span data-ttu-id="b1a53-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="b1a53-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="b1a53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1a53-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a53-103">Register-AzStackHCI skapar en Microsoft. AzureStackHCI-moln resurs som representerar det lokala klustret och registrerar det lokala klustret med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a53-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="b1a53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1a53-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="b1a53-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1a53-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a53-106">Register-AzStackHCI skapar en Microsoft. AzureStackHCI-moln resurs som representerar det lokala klustret och registrerar det lokala klustret med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a53-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="b1a53-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1a53-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a53-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="b1a53-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="b1a53-109">C:\PS \> register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" resultat: lyckades ResourceID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="b1a53-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="b1a53-110">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="b1a53-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="b1a53-111">C:\PS \> register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ComputerName ClusterNode1 result: lyckades ResourceID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="b1a53-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="b1a53-112">EXEMPEL 3</span><span class="sxs-lookup"><span data-stu-id="b1a53-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="b1a53-113">C:\PS \> register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -regionen West-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG result: PendingForAdminConsent ResourceID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="b1a53-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="b1a53-114">EXEMPEL 4</span><span class="sxs-lookup"><span data-stu-id="b1a53-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="b1a53-115">C:\PS \> register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-regionen West-resourceName HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken Acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-ComputerName node1hci-Credential Get-Credential result: lyckades ResourceID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="b1a53-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="b1a53-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1a53-116">PARAMETERS</span></span>

### <span data-ttu-id="b1a53-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="b1a53-117">-AccountId</span></span>
<span data-ttu-id="b1a53-118">Anger ARM-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="b1a53-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="b1a53-119">Genom att ange detta tillsammans med ArmAccessToken och GraphAccessToken undviker du Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="b1a53-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a53-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="b1a53-120">-ArmAccessToken</span></span>
<span data-ttu-id="b1a53-121">Anger ARM-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="b1a53-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="b1a53-122">Om du anger detta tillsammans med GraphAccessToken och AccountId undviks Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="b1a53-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="b1a53-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b1a53-123">-CertificateThumbprint</span></span>
<span data-ttu-id="b1a53-124">Anger tumavtrycket för det certifikat som är tillgängligt på alla noder.</span><span class="sxs-lookup"><span data-stu-id="b1a53-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="b1a53-125">Användaren ansvarar för att hantera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b1a53-125">User is responsible for managing the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a53-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="b1a53-126">-ComputerName</span></span>
<span data-ttu-id="b1a53-127">Anger kluster namnet eller en av klusternoderna i det lokala klustret som registreras på Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a53-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a53-128">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="b1a53-128">-Credential</span></span>
<span data-ttu-id="b1a53-129">Anger autentiseringsuppgifter för dator namnet.</span><span class="sxs-lookup"><span data-stu-id="b1a53-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="b1a53-130">Standard är den aktuella användaren som kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1a53-130">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a53-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b1a53-131">-EnvironmentName</span></span>
<span data-ttu-id="b1a53-132">Anger Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="b1a53-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="b1a53-133">Standard är AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="b1a53-133">Default is AzureCloud.</span></span>
<span data-ttu-id="b1a53-134">Giltiga värden är AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="b1a53-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a53-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="b1a53-135">-GraphAccessToken</span></span>
<span data-ttu-id="b1a53-136">Anger Graph-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="b1a53-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="b1a53-137">Om du anger detta tillsammans med ArmAccessToken och AccountId undviks Azure interaktiv inloggning.</span><span class="sxs-lookup"><span data-stu-id="b1a53-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="b1a53-138">-Region</span><span class="sxs-lookup"><span data-stu-id="b1a53-138">-Region</span></span>
<span data-ttu-id="b1a53-139">Anger region för att skapa resursen.</span><span class="sxs-lookup"><span data-stu-id="b1a53-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="b1a53-140">Standardvärdet är öster.</span><span class="sxs-lookup"><span data-stu-id="b1a53-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="b1a53-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="b1a53-141">-RepairRegistration</span></span>
<span data-ttu-id="b1a53-142">Reparera den aktuella Azure Stack HCI-registreringen med molnet.</span><span class="sxs-lookup"><span data-stu-id="b1a53-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="b1a53-143">Denna cmdlet tar bort de lokala certifikaten på de klustrade noderna och fjärrcertifikaten i Azure AD-programmet i molnet och skapar nya ersättnings certifikat för båda.</span><span class="sxs-lookup"><span data-stu-id="b1a53-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="b1a53-144">Resurs gruppen, resurs namnet och andra registrerings alternativ bevaras.</span><span class="sxs-lookup"><span data-stu-id="b1a53-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="b1a53-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a53-145">-ResourceGroupName</span></span>
<span data-ttu-id="b1a53-146">Anger namnet på Azure Resource-gruppen.</span><span class="sxs-lookup"><span data-stu-id="b1a53-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="b1a53-147">Om ej angivet \<LocalClusterName\> -RG kommer att användas som resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b1a53-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="b1a53-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b1a53-148">-ResourceName</span></span>
<span data-ttu-id="b1a53-149">Anger resurs namnet på resursen som har skapats i Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a53-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="b1a53-150">Om det inte anges används det lokala kluster namnet.</span><span class="sxs-lookup"><span data-stu-id="b1a53-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="b1a53-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1a53-151">-SubscriptionId</span></span>
<span data-ttu-id="b1a53-152">Anger Azure-abonnemanget för att skapa resursen.</span><span class="sxs-lookup"><span data-stu-id="b1a53-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="b1a53-153">Det här är den enda obligatoriska parametern.</span><span class="sxs-lookup"><span data-stu-id="b1a53-153">This is the only Mandatory parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a53-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b1a53-154">-TenantId</span></span>
<span data-ttu-id="b1a53-155">Anger Azure TenantId.</span><span class="sxs-lookup"><span data-stu-id="b1a53-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="b1a53-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="b1a53-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="b1a53-157">Använd enhets kod i stället för en interaktiv webbläsare.</span><span class="sxs-lookup"><span data-stu-id="b1a53-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="b1a53-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a53-158">CommonParameters</span></span>
<span data-ttu-id="b1a53-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a53-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a53-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1a53-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a53-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1a53-161">INPUTS</span></span>

## <span data-ttu-id="b1a53-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1a53-162">OUTPUTS</span></span>

### <span data-ttu-id="b1a53-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="b1a53-163">PSCustomObject.</span></span> <span data-ttu-id="b1a53-164">Returnerar följande egenskaper i PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="b1a53-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="b1a53-165">Resultat: lyckades eller misslyckades eller PendingForAdminConsent eller avbröts.</span><span class="sxs-lookup"><span data-stu-id="b1a53-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="b1a53-166">ResourceId: resurs-ID för resursen som har skapats i Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a53-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="b1a53-167">PortalResourceURL: URL för Azure Portal resurs.</span><span class="sxs-lookup"><span data-stu-id="b1a53-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="b1a53-168">PortalAADAppPermissionsURL: URL-adressen till webbplatsen för webbplatsens program behörigheter.</span><span class="sxs-lookup"><span data-stu-id="b1a53-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="b1a53-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1a53-169">NOTES</span></span>

## <span data-ttu-id="b1a53-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1a53-170">RELATED LINKS</span></span>
