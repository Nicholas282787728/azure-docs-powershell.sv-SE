---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 30635aa9bc1906c9e329e605327df1a2dfce5df4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574331"
---
# <span data-ttu-id="f8d9f-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f8d9f-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="f8d9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d9f-103">Skapar en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8d9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8d9f-104">SYNTAX</span></span>

### <span data-ttu-id="f8d9f-105">CreateContainerGroupBaseParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f8d9f-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d9f-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="f8d9f-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d9f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8d9f-107">DESCRIPTION</span></span>
<span data-ttu-id="f8d9f-108">Cmdleten **New-AzureRmContainerGroup** skapar en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="f8d9f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8d9f-109">EXAMPLES</span></span>

### <span data-ttu-id="f8d9f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f8d9f-110">Example 1</span></span>
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

<span data-ttu-id="f8d9f-111">Med de här kommandona skapas en behållar grupp med den senaste nginx-bilden och begär en offentlig IP-adress med öppning av port 8000</span><span class="sxs-lookup"><span data-stu-id="f8d9f-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="f8d9f-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f8d9f-112">Example 2</span></span>
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

<span data-ttu-id="f8d9f-113">De här kommandona skapar en behållar grupp och kör ett anpassat skript i behållaren.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="f8d9f-114">Exempel 3: skapa en behållare för en slut för ande tjänst.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-114">Example 3: Creates a run-to-completion container group.</span></span>
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

<span data-ttu-id="f8d9f-115">De här kommandona skapar en behållar grupp som skriver ut ' Hej ' och slutar.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="f8d9f-116">Exempel 4: skapar en behållar grupp med hjälp av bild i Azure-behållarobjekt</span><span class="sxs-lookup"><span data-stu-id="f8d9f-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
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

<span data-ttu-id="f8d9f-117">Det här kommandot skapar en behållar grupp med hjälp av en nginx-bild i Azure Container-registret.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="f8d9f-118">Exempel 5: skapar en behållar grupp med hjälp av bild i eget register för behållar bilder</span><span class="sxs-lookup"><span data-stu-id="f8d9f-118">Example 5: Creates a container group using image in custom container image registry</span></span>
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

<span data-ttu-id="f8d9f-119">Med de här kommandona skapas en behållar grupp med hjälp av en anpassad bild från ett eget register för en behållare.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="f8d9f-120">Exempel 6: skapar en behållar grupp som monterar Azure-filvolymen</span><span class="sxs-lookup"><span data-stu-id="f8d9f-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
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

<span data-ttu-id="f8d9f-121">De här kommandona skapar en behållar grupp som monterar den tillhandahållna Azure-fildelningen `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="f8d9f-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="f8d9f-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8d9f-122">PARAMETERS</span></span>

### <span data-ttu-id="f8d9f-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f8d9f-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="f8d9f-124">Autentiseringsuppgifterna för lagrings kontot för Azure-fildelningen för att montera där användar namnet är lagrings kontots namn och nycklar är lagrings kontots fil.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="f8d9f-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="f8d9f-126">Monterings vägen för Azure-filvolymen.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="f8d9f-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="f8d9f-128">Namnet på den Azure-fildelning du vill montera.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-129">-Kommando</span><span class="sxs-lookup"><span data-stu-id="f8d9f-129">-Command</span></span>
<span data-ttu-id="f8d9f-130">Kommandot som ska köras i behållaren.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-130">The command to run in the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-131">-CPU</span><span class="sxs-lookup"><span data-stu-id="f8d9f-131">-Cpu</span></span>
<span data-ttu-id="f8d9f-132">Nödvändiga CPU-kärnor.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-132">The required CPU cores.</span></span>
<span data-ttu-id="f8d9f-133">Standard: 1</span><span class="sxs-lookup"><span data-stu-id="f8d9f-133">Default: 1</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d9f-134">-DefaultProfile</span></span>
<span data-ttu-id="f8d9f-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="f8d9f-136">-DnsNameLabel</span></span>
<span data-ttu-id="f8d9f-137">DNS-namnets etikett för IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-137">The DNS name label for the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="f8d9f-138">-EnvironmentVariable</span></span>
<span data-ttu-id="f8d9f-139">Variabler för behållar miljön.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-139">The container environment variables.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-140">-Image</span><span class="sxs-lookup"><span data-stu-id="f8d9f-140">-Image</span></span>
<span data-ttu-id="f8d9f-141">Behållar bilden.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-141">The container image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-142">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="f8d9f-142">-IpAddressType</span></span>
<span data-ttu-id="f8d9f-143">IP-adress typen.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-143">The IP address type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-144">-Plats</span><span class="sxs-lookup"><span data-stu-id="f8d9f-144">-Location</span></span>
<span data-ttu-id="f8d9f-145">Plats för behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-145">The container group Location.</span></span>
<span data-ttu-id="f8d9f-146">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-146">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="f8d9f-147">-MemoryInGB</span></span>
<span data-ttu-id="f8d9f-148">Det nödvändiga minnet i GB.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-148">The required memory in GB.</span></span>
<span data-ttu-id="f8d9f-149">Standard: 1,5</span><span class="sxs-lookup"><span data-stu-id="f8d9f-149">Default: 1.5</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8d9f-150">-Name</span></span>
<span data-ttu-id="f8d9f-151">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-151">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="f8d9f-152">-OsType</span></span>
<span data-ttu-id="f8d9f-153">OS-typen för behållaren.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-153">The container OS type.</span></span>
<span data-ttu-id="f8d9f-154">Standard: Linux</span><span class="sxs-lookup"><span data-stu-id="f8d9f-154">Default: Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-155">-Port</span><span class="sxs-lookup"><span data-stu-id="f8d9f-155">-Port</span></span>
<span data-ttu-id="f8d9f-156">De portar som ska öppnas.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-156">The port(s) to open.</span></span> <span data-ttu-id="f8d9f-157">Standard: [80]</span><span class="sxs-lookup"><span data-stu-id="f8d9f-157">Default: [80]</span></span>

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="f8d9f-158">-RegistryCredential</span></span>
<span data-ttu-id="f8d9f-159">Den anpassade autentiseringsuppgiften för container-registret.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-159">The custom container registry credential.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="f8d9f-160">-RegistryServerDomain</span></span>
<span data-ttu-id="f8d9f-161">Den anpassade inloggnings servern för en behållare.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-161">The custom container registry login server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d9f-162">-ResourceGroupName</span></span>
<span data-ttu-id="f8d9f-163">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-163">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="f8d9f-164">-RestartPolicy</span></span>
<span data-ttu-id="f8d9f-165">Restart-principen för container.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-165">The container restart policy.</span></span> <span data-ttu-id="f8d9f-166">Standard: alltid</span><span class="sxs-lookup"><span data-stu-id="f8d9f-166">Default: Always</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-167">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f8d9f-167">-Tag</span></span>
<span data-ttu-id="f8d9f-168">{{Fill tag Description}}</span><span class="sxs-lookup"><span data-stu-id="f8d9f-168">{{Fill Tag Description}}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d9f-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8d9f-169">-Confirm</span></span>
<span data-ttu-id="f8d9f-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d9f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d9f-171">-WhatIf</span></span>
<span data-ttu-id="f8d9f-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d9f-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d9f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d9f-174">CommonParameters</span></span>
<span data-ttu-id="f8d9f-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d9f-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8d9f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d9f-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8d9f-177">INPUTS</span></span>

### <span data-ttu-id="f8d9f-178">System. String</span><span class="sxs-lookup"><span data-stu-id="f8d9f-178">System.String</span></span>
<span data-ttu-id="f8d9f-179">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f8d9f-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f8d9f-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8d9f-180">OUTPUTS</span></span>

### <span data-ttu-id="f8d9f-181">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f8d9f-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="f8d9f-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8d9f-182">NOTES</span></span>

## <span data-ttu-id="f8d9f-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8d9f-183">RELATED LINKS</span></span>
