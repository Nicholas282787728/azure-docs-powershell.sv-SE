---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 1823759b72bdb3162164068732f3a8201fcfb589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573988"
---
# <span data-ttu-id="3d40c-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3d40c-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="3d40c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d40c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d40c-103">Skapar en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="3d40c-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d40c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d40c-104">SYNTAX</span></span>

### <span data-ttu-id="3d40c-105">CreateContainerGroupBaseParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3d40c-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d40c-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="3d40c-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d40c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d40c-107">DESCRIPTION</span></span>
<span data-ttu-id="3d40c-108">Cmdleten **New-AzureRmContainerGroup** skapar en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="3d40c-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="3d40c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d40c-109">EXAMPLES</span></span>

### <span data-ttu-id="3d40c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d40c-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="3d40c-111">Med de här kommandona skapas en behållar grupp med den senaste nginx-bilden och begär en offentlig IP-adress med öppning av port 8000</span><span class="sxs-lookup"><span data-stu-id="3d40c-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="3d40c-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3d40c-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="3d40c-113">De här kommandona skapar en behållar grupp och kör ett anpassat skript i behållaren.</span><span class="sxs-lookup"><span data-stu-id="3d40c-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="3d40c-114">Exempel 3: skapa en behållare för en slut för ande tjänst.</span><span class="sxs-lookup"><span data-stu-id="3d40c-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="3d40c-115">De här kommandona skapar en behållar grupp som skriver ut ' Hej ' och slutar.</span><span class="sxs-lookup"><span data-stu-id="3d40c-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="3d40c-116">Exempel 4: skapar en behållar grupp med hjälp av bild i Azure-behållarobjekt</span><span class="sxs-lookup"><span data-stu-id="3d40c-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="3d40c-117">Det här kommandot skapar en behållar grupp med hjälp av en nginx-bild i Azure Container-registret.</span><span class="sxs-lookup"><span data-stu-id="3d40c-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="3d40c-118">Exempel 5: skapar en behållar grupp med hjälp av bild i eget register för behållar bilder</span><span class="sxs-lookup"><span data-stu-id="3d40c-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="3d40c-119">Med de här kommandona skapas en behållar grupp med hjälp av en anpassad bild från ett eget register för en behållare.</span><span class="sxs-lookup"><span data-stu-id="3d40c-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="3d40c-120">Exempel 6: skapar en behållar grupp som monterar Azure-filvolymen</span><span class="sxs-lookup"><span data-stu-id="3d40c-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="3d40c-121">De här kommandona skapar en behållar grupp som monterar den tillhandahållna Azure-fildelningen `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="3d40c-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="3d40c-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d40c-122">PARAMETERS</span></span>

### <span data-ttu-id="3d40c-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3d40c-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="3d40c-124">Autentiseringsuppgifterna för lagrings kontot för Azure-fildelningen för att montera där användar namnet är lagrings kontots namn och nycklar är lagrings kontots fil.</span><span class="sxs-lookup"><span data-stu-id="3d40c-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d40c-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="3d40c-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="3d40c-126">Monterings vägen för Azure-filvolymen.</span><span class="sxs-lookup"><span data-stu-id="3d40c-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d40c-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="3d40c-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="3d40c-128">Namnet på den Azure-fildelning du vill montera.</span><span class="sxs-lookup"><span data-stu-id="3d40c-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d40c-129">-Kommando</span><span class="sxs-lookup"><span data-stu-id="3d40c-129">-Command</span></span>
<span data-ttu-id="3d40c-130">Kommandot som ska köras i behållaren.</span><span class="sxs-lookup"><span data-stu-id="3d40c-130">The command to run in the container.</span></span>

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

### <span data-ttu-id="3d40c-131">-CPU</span><span class="sxs-lookup"><span data-stu-id="3d40c-131">-Cpu</span></span>
<span data-ttu-id="3d40c-132">Nödvändiga CPU-kärnor.</span><span class="sxs-lookup"><span data-stu-id="3d40c-132">The required CPU cores.</span></span>
<span data-ttu-id="3d40c-133">Standard: 1</span><span class="sxs-lookup"><span data-stu-id="3d40c-133">Default: 1</span></span>

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

### <span data-ttu-id="3d40c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d40c-134">-DefaultProfile</span></span>
<span data-ttu-id="3d40c-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d40c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d40c-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="3d40c-136">-DnsNameLabel</span></span>
<span data-ttu-id="3d40c-137">DNS-namnets etikett för IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="3d40c-137">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="3d40c-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="3d40c-138">-EnvironmentVariable</span></span>
<span data-ttu-id="3d40c-139">Variabler för behållar miljön.</span><span class="sxs-lookup"><span data-stu-id="3d40c-139">The container environment variables.</span></span>

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

### <span data-ttu-id="3d40c-140">-Image</span><span class="sxs-lookup"><span data-stu-id="3d40c-140">-Image</span></span>
<span data-ttu-id="3d40c-141">Behållar bilden.</span><span class="sxs-lookup"><span data-stu-id="3d40c-141">The container image.</span></span>

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

### <span data-ttu-id="3d40c-142">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="3d40c-142">-IpAddressType</span></span>
<span data-ttu-id="3d40c-143">IP-adress typen.</span><span class="sxs-lookup"><span data-stu-id="3d40c-143">The IP address type.</span></span>

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

### <span data-ttu-id="3d40c-144">-Plats</span><span class="sxs-lookup"><span data-stu-id="3d40c-144">-Location</span></span>
<span data-ttu-id="3d40c-145">Plats för behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d40c-145">The container group Location.</span></span>
<span data-ttu-id="3d40c-146">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d40c-146">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="3d40c-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="3d40c-147">-MemoryInGB</span></span>
<span data-ttu-id="3d40c-148">Det nödvändiga minnet i GB.</span><span class="sxs-lookup"><span data-stu-id="3d40c-148">The required memory in GB.</span></span>
<span data-ttu-id="3d40c-149">Standard: 1,5</span><span class="sxs-lookup"><span data-stu-id="3d40c-149">Default: 1.5</span></span>

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

### <span data-ttu-id="3d40c-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d40c-150">-Name</span></span>
<span data-ttu-id="3d40c-151">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d40c-151">The container group name.</span></span>

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

### <span data-ttu-id="3d40c-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="3d40c-152">-OsType</span></span>
<span data-ttu-id="3d40c-153">OS-typen för behållaren.</span><span class="sxs-lookup"><span data-stu-id="3d40c-153">The container OS type.</span></span>
<span data-ttu-id="3d40c-154">Standard: Linux</span><span class="sxs-lookup"><span data-stu-id="3d40c-154">Default: Linux</span></span>

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

### <span data-ttu-id="3d40c-155">-Port</span><span class="sxs-lookup"><span data-stu-id="3d40c-155">-Port</span></span>
<span data-ttu-id="3d40c-156">De portar som ska öppnas.</span><span class="sxs-lookup"><span data-stu-id="3d40c-156">The port(s) to open.</span></span> <span data-ttu-id="3d40c-157">Standard: [80]</span><span class="sxs-lookup"><span data-stu-id="3d40c-157">Default: [80]</span></span>

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

### <span data-ttu-id="3d40c-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="3d40c-158">-RegistryCredential</span></span>
<span data-ttu-id="3d40c-159">Den anpassade autentiseringsuppgiften för container-registret.</span><span class="sxs-lookup"><span data-stu-id="3d40c-159">The custom container registry credential.</span></span>

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

### <span data-ttu-id="3d40c-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="3d40c-160">-RegistryServerDomain</span></span>
<span data-ttu-id="3d40c-161">Den anpassade inloggnings servern för en behållare.</span><span class="sxs-lookup"><span data-stu-id="3d40c-161">The custom container registry login server.</span></span>

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

### <span data-ttu-id="3d40c-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d40c-162">-ResourceGroupName</span></span>
<span data-ttu-id="3d40c-163">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3d40c-163">The resource group name.</span></span>

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

### <span data-ttu-id="3d40c-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="3d40c-164">-RestartPolicy</span></span>
<span data-ttu-id="3d40c-165">Restart-principen för container.</span><span class="sxs-lookup"><span data-stu-id="3d40c-165">The container restart policy.</span></span> <span data-ttu-id="3d40c-166">Standard: alltid</span><span class="sxs-lookup"><span data-stu-id="3d40c-166">Default: Always</span></span>

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

### <span data-ttu-id="3d40c-167">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3d40c-167">-Tag</span></span>
<span data-ttu-id="3d40c-168">{{Fill tag Description}}</span><span class="sxs-lookup"><span data-stu-id="3d40c-168">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="3d40c-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d40c-169">-Confirm</span></span>
<span data-ttu-id="3d40c-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d40c-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d40c-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d40c-171">-WhatIf</span></span>
<span data-ttu-id="3d40c-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d40c-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d40c-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d40c-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d40c-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d40c-174">CommonParameters</span></span>
<span data-ttu-id="3d40c-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d40c-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d40c-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d40c-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d40c-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d40c-177">INPUTS</span></span>

### <span data-ttu-id="3d40c-178">System. String</span><span class="sxs-lookup"><span data-stu-id="3d40c-178">System.String</span></span>

### <span data-ttu-id="3d40c-179">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3d40c-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d40c-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d40c-180">OUTPUTS</span></span>

### <span data-ttu-id="3d40c-181">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3d40c-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="3d40c-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d40c-182">NOTES</span></span>

## <span data-ttu-id="3d40c-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d40c-183">RELATED LINKS</span></span>
