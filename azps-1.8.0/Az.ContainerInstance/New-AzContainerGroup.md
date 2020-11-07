---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 76719250ca7909d86d288b987b9598a58ab5fb88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754420"
---
# <span data-ttu-id="4b307-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4b307-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="4b307-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b307-102">SYNOPSIS</span></span>
<span data-ttu-id="4b307-103">Skapar en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="4b307-103">Creates a container group.</span></span>

## <span data-ttu-id="4b307-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b307-104">SYNTAX</span></span>

### <span data-ttu-id="4b307-105">CreateContainerGroupBaseParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4b307-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b307-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="4b307-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b307-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="4b307-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b307-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b307-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b307-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b307-109">DESCRIPTION</span></span>
<span data-ttu-id="4b307-110">Cmdleten **New-AzContainerGroup** skapar en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="4b307-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="4b307-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b307-111">EXAMPLES</span></span>

### <span data-ttu-id="4b307-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4b307-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="4b307-113">Med de här kommandona skapas en behållar grupp med den senaste nginx-bilden och begär en offentlig IP-adress med öppning av port 8000</span><span class="sxs-lookup"><span data-stu-id="4b307-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="4b307-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4b307-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="4b307-115">De här kommandona skapar en behållar grupp och kör ett anpassat skript i behållaren.</span><span class="sxs-lookup"><span data-stu-id="4b307-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="4b307-116">Exempel 3: skapa en behållare för en slut för ande tjänst.</span><span class="sxs-lookup"><span data-stu-id="4b307-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="4b307-117">De här kommandona skapar en behållar grupp som skriver ut ' Hej ' och slutar.</span><span class="sxs-lookup"><span data-stu-id="4b307-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="4b307-118">Exempel 4: skapar en behållar grupp med hjälp av bild i Azure-behållarobjekt</span><span class="sxs-lookup"><span data-stu-id="4b307-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="4b307-119">Det här kommandot skapar en behållar grupp med hjälp av en nginx-bild i Azure Container-registret.</span><span class="sxs-lookup"><span data-stu-id="4b307-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="4b307-120">Exempel 5: skapar en behållar grupp med hjälp av bild i eget register för behållar bilder</span><span class="sxs-lookup"><span data-stu-id="4b307-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="4b307-121">Med de här kommandona skapas en behållar grupp med hjälp av en anpassad bild från ett eget register för en behållare.</span><span class="sxs-lookup"><span data-stu-id="4b307-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="4b307-122">Exempel 6: skapar en behållar grupp som monterar Azure-filvolymen</span><span class="sxs-lookup"><span data-stu-id="4b307-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzFileVolumeShareName myshare -AzFileVolumeAccountKey $mycred -AzFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="4b307-123">De här kommandona skapar en behållar grupp som monterar den tillhandahållna Azure-fildelningen `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="4b307-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="4b307-124">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="4b307-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="4b307-125">Det här kommandot skapar en behållar grupp med en tilldelad identitet med den senaste nginx-avbildningen och begär en offentlig IP-adress med öppning av port 8000</span><span class="sxs-lookup"><span data-stu-id="4b307-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="4b307-126">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="4b307-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="4b307-127">Med de här kommandona skapas en behållar grupp med tilldelad och användardefinierad identitet med den senaste nginx-avbildningen och begär en offentlig IP-adress med öppning av port 8000.</span><span class="sxs-lookup"><span data-stu-id="4b307-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="4b307-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b307-128">PARAMETERS</span></span>

### <span data-ttu-id="4b307-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4b307-129">-AssignIdentity</span></span>
<span data-ttu-id="4b307-130">Aktivera tilldelad identitet</span><span class="sxs-lookup"><span data-stu-id="4b307-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4b307-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="4b307-132">Autentiseringsuppgifterna för lagrings kontot för Azure-fildelningen för att montera där användar namnet är lagrings kontots namn och nycklar är lagrings kontots fil.</span><span class="sxs-lookup"><span data-stu-id="4b307-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="4b307-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="4b307-134">Monterings vägen för Azure-filvolymen.</span><span class="sxs-lookup"><span data-stu-id="4b307-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="4b307-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="4b307-136">Namnet på den Azure-fildelning du vill montera.</span><span class="sxs-lookup"><span data-stu-id="4b307-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-137">-Kommando</span><span class="sxs-lookup"><span data-stu-id="4b307-137">-Command</span></span>
<span data-ttu-id="4b307-138">Kommandot som ska köras i behållaren.</span><span class="sxs-lookup"><span data-stu-id="4b307-138">The command to run in the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-139">-CPU</span><span class="sxs-lookup"><span data-stu-id="4b307-139">-Cpu</span></span>
<span data-ttu-id="4b307-140">Nödvändiga CPU-kärnor.</span><span class="sxs-lookup"><span data-stu-id="4b307-140">The required CPU cores.</span></span>
<span data-ttu-id="4b307-141">Standard: 1</span><span class="sxs-lookup"><span data-stu-id="4b307-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b307-142">-DefaultProfile</span></span>
<span data-ttu-id="4b307-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b307-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b307-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="4b307-144">-DnsNameLabel</span></span>
<span data-ttu-id="4b307-145">DNS-namnets etikett för IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="4b307-145">The DNS name label for the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="4b307-146">-EnvironmentVariable</span></span>
<span data-ttu-id="4b307-147">Variabler för behållar miljön.</span><span class="sxs-lookup"><span data-stu-id="4b307-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4b307-148">-IdentityId</span></span>
<span data-ttu-id="4b307-149">Användarens tilldelade ID-nummer</span><span class="sxs-lookup"><span data-stu-id="4b307-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4b307-150">-IdentityType</span></span>
<span data-ttu-id="4b307-151">Den hanterade identitets typen</span><span class="sxs-lookup"><span data-stu-id="4b307-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-152">-Image</span><span class="sxs-lookup"><span data-stu-id="4b307-152">-Image</span></span>
<span data-ttu-id="4b307-153">Behållar bilden.</span><span class="sxs-lookup"><span data-stu-id="4b307-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="4b307-154">-IpAddressType</span></span>
<span data-ttu-id="4b307-155">IP-adress typen.</span><span class="sxs-lookup"><span data-stu-id="4b307-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-156">-Plats</span><span class="sxs-lookup"><span data-stu-id="4b307-156">-Location</span></span>
<span data-ttu-id="4b307-157">Plats för behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="4b307-157">The container group Location.</span></span>
<span data-ttu-id="4b307-158">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4b307-158">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="4b307-159">-MemoryInGB</span></span>
<span data-ttu-id="4b307-160">Det nödvändiga minnet i GB.</span><span class="sxs-lookup"><span data-stu-id="4b307-160">The required memory in GB.</span></span>
<span data-ttu-id="4b307-161">Standard: 1,5</span><span class="sxs-lookup"><span data-stu-id="4b307-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-162">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b307-162">-Name</span></span>
<span data-ttu-id="4b307-163">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="4b307-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="4b307-164">-OsType</span></span>
<span data-ttu-id="4b307-165">OS-typen för behållaren.</span><span class="sxs-lookup"><span data-stu-id="4b307-165">The container OS type.</span></span>
<span data-ttu-id="4b307-166">Standard: Linux</span><span class="sxs-lookup"><span data-stu-id="4b307-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-167">-Port</span><span class="sxs-lookup"><span data-stu-id="4b307-167">-Port</span></span>
<span data-ttu-id="4b307-168">De portar som ska öppnas.</span><span class="sxs-lookup"><span data-stu-id="4b307-168">The port(s) to open.</span></span> <span data-ttu-id="4b307-169">Standard: [80]</span><span class="sxs-lookup"><span data-stu-id="4b307-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4b307-170">-RegistryCredential</span></span>
<span data-ttu-id="4b307-171">Den anpassade autentiseringsuppgiften för container-registret.</span><span class="sxs-lookup"><span data-stu-id="4b307-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="4b307-172">-RegistryServerDomain</span></span>
<span data-ttu-id="4b307-173">Den anpassade inloggnings servern för en behållare.</span><span class="sxs-lookup"><span data-stu-id="4b307-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b307-174">-ResourceGroupName</span></span>
<span data-ttu-id="4b307-175">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4b307-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="4b307-176">-RestartPolicy</span></span>
<span data-ttu-id="4b307-177">Restart-principen för container.</span><span class="sxs-lookup"><span data-stu-id="4b307-177">The container restart policy.</span></span> <span data-ttu-id="4b307-178">Standard: alltid</span><span class="sxs-lookup"><span data-stu-id="4b307-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-179">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4b307-179">-Tag</span></span>
<span data-ttu-id="4b307-180">{{Fill tag Description}}</span><span class="sxs-lookup"><span data-stu-id="4b307-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b307-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b307-181">-Confirm</span></span>
<span data-ttu-id="4b307-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b307-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b307-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b307-183">-WhatIf</span></span>
<span data-ttu-id="4b307-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b307-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b307-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b307-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b307-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b307-186">CommonParameters</span></span>
<span data-ttu-id="4b307-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b307-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b307-188">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b307-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b307-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b307-189">INPUTS</span></span>

### <span data-ttu-id="4b307-190">System. String</span><span class="sxs-lookup"><span data-stu-id="4b307-190">System.String</span></span>

### <span data-ttu-id="4b307-191">System. string []</span><span class="sxs-lookup"><span data-stu-id="4b307-191">System.String[]</span></span>

### <span data-ttu-id="4b307-192">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4b307-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4b307-193">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b307-193">OUTPUTS</span></span>

### <span data-ttu-id="4b307-194">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4b307-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="4b307-195">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b307-195">NOTES</span></span>

## <span data-ttu-id="4b307-196">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b307-196">RELATED LINKS</span></span>
