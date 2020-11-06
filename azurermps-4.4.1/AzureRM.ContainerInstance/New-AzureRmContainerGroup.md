---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582500"
---
# <span data-ttu-id="b3a7b-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b3a7b-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="b3a7b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a7b-103">Skapar en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3a7b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3a7b-104">SYNTAX</span></span>

### <span data-ttu-id="b3a7b-105">CreateContainerGroupBaseParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b3a7b-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a7b-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="b3a7b-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3a7b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3a7b-107">DESCRIPTION</span></span>
<span data-ttu-id="b3a7b-108">Cmdleten **New-AzureRmContainerGroup** skapar en behållar grupp.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="b3a7b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3a7b-109">EXAMPLES</span></span>

### <span data-ttu-id="b3a7b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b3a7b-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="b3a7b-111">Med de här kommandona skapas en behållar grupp med den senaste nginx-bilden och begär en offentlig IP-adress med öppning av port 8000</span><span class="sxs-lookup"><span data-stu-id="b3a7b-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="b3a7b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b3a7b-112">Example 2</span></span>
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
```

<span data-ttu-id="b3a7b-113">De här kommandona skapar en behållar grupp och kör ett anpassat skript i behållaren.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="b3a7b-114">Exempel 3: skapar en behållar grupp med hjälp av bild i Azure-behållarobjekt</span><span class="sxs-lookup"><span data-stu-id="b3a7b-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
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
```

<span data-ttu-id="b3a7b-115">Det här kommandot skapar en behållar grupp med hjälp av en nginx-bild i Azure Container-registret.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="b3a7b-116">Exempel 4: skapar en behållar grupp med hjälp av bild i eget register för behållar bilder</span><span class="sxs-lookup"><span data-stu-id="b3a7b-116">Example 4: Creates a container group using image in custom container image registry</span></span>
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
```

<span data-ttu-id="b3a7b-117">Med de här kommandona skapas en behållar grupp med hjälp av en anpassad bild från ett eget register för en behållare.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="b3a7b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3a7b-118">PARAMETERS</span></span>

### <span data-ttu-id="b3a7b-119">-Kommando</span><span class="sxs-lookup"><span data-stu-id="b3a7b-119">-Command</span></span>
<span data-ttu-id="b3a7b-120">Kommandot som ska köras i behållaren.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="b3a7b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b3a7b-121">-Confirm</span></span>
<span data-ttu-id="b3a7b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a7b-123">-CPU</span><span class="sxs-lookup"><span data-stu-id="b3a7b-123">-Cpu</span></span>
<span data-ttu-id="b3a7b-124">Nödvändiga CPU-kärnor.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-124">The required CPU cores.</span></span>
<span data-ttu-id="b3a7b-125">Standard: 1</span><span class="sxs-lookup"><span data-stu-id="b3a7b-125">Default: 1</span></span>

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

### <span data-ttu-id="b3a7b-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="b3a7b-126">-EnvironmentVariable</span></span>
<span data-ttu-id="b3a7b-127">Variabler för behållar miljön.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-127">The container environment variables.</span></span>

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

### <span data-ttu-id="b3a7b-128">-Image</span><span class="sxs-lookup"><span data-stu-id="b3a7b-128">-Image</span></span>
<span data-ttu-id="b3a7b-129">Behållar bilden.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-129">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a7b-130">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="b3a7b-130">-IpAddressType</span></span>
<span data-ttu-id="b3a7b-131">IP-adress typen.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-131">The IP address type.</span></span>

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

### <span data-ttu-id="b3a7b-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="b3a7b-132">-Location</span></span>
<span data-ttu-id="b3a7b-133">Plats för behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-133">The container group Location.</span></span>
<span data-ttu-id="b3a7b-134">Standard platsen för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="b3a7b-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="b3a7b-135">-MemoryInGB</span></span>
<span data-ttu-id="b3a7b-136">Det nödvändiga minnet i GB.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-136">The required memory in GB.</span></span>
<span data-ttu-id="b3a7b-137">Standard: 1,5</span><span class="sxs-lookup"><span data-stu-id="b3a7b-137">Default: 1.5</span></span>

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

### <span data-ttu-id="b3a7b-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3a7b-138">-Name</span></span>
<span data-ttu-id="b3a7b-139">Namn på behållar gruppen.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-139">The container group name.</span></span>

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

### <span data-ttu-id="b3a7b-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="b3a7b-140">-OsType</span></span>
<span data-ttu-id="b3a7b-141">OS-typen för behållaren.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-141">The container OS type.</span></span>
<span data-ttu-id="b3a7b-142">Standard: Linux</span><span class="sxs-lookup"><span data-stu-id="b3a7b-142">Default: Linux</span></span>

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

### <span data-ttu-id="b3a7b-143">-Port</span><span class="sxs-lookup"><span data-stu-id="b3a7b-143">-Port</span></span>
<span data-ttu-id="b3a7b-144">Porten som ska öppnas.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-144">The port to open.</span></span>
<span data-ttu-id="b3a7b-145">Standard: 80</span><span class="sxs-lookup"><span data-stu-id="b3a7b-145">Default: 80</span></span>

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

### <span data-ttu-id="b3a7b-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="b3a7b-146">-RegistryCredential</span></span>
<span data-ttu-id="b3a7b-147">Den anpassade autentiseringsuppgiften för container-registret.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a7b-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="b3a7b-148">-RegistryServerDomain</span></span>
<span data-ttu-id="b3a7b-149">Den anpassade inloggnings servern för en behållare.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a7b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a7b-150">-ResourceGroupName</span></span>
<span data-ttu-id="b3a7b-151">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-151">The resource group name.</span></span>

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

### <span data-ttu-id="b3a7b-152">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b3a7b-152">-Tag</span></span>
<span data-ttu-id="b3a7b-153">{{Fill tag Description}}</span><span class="sxs-lookup"><span data-stu-id="b3a7b-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="b3a7b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a7b-154">-WhatIf</span></span>
<span data-ttu-id="b3a7b-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a7b-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a7b-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a7b-157">-DefaultProfile</span></span>
<span data-ttu-id="b3a7b-158">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3a7b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a7b-159">CommonParameters</span></span>
<span data-ttu-id="b3a7b-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a7b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a7b-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3a7b-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a7b-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3a7b-162">INPUTS</span></span>

### <span data-ttu-id="b3a7b-163">System. String</span><span class="sxs-lookup"><span data-stu-id="b3a7b-163">System.String</span></span>
<span data-ttu-id="b3a7b-164">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b3a7b-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b3a7b-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3a7b-165">OUTPUTS</span></span>

### <span data-ttu-id="b3a7b-166">Microsoft. Azure. commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="b3a7b-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="b3a7b-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3a7b-167">NOTES</span></span>

## <span data-ttu-id="b3a7b-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3a7b-168">RELATED LINKS</span></span>

