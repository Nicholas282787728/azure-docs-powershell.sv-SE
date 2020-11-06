---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 51ebdbffcb88c1d43716170b236332741d05466f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580275"
---
# <span data-ttu-id="fdbd9-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="fdbd9-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="fdbd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbd9-103">Skapar ett lokalt konfigurations objekt för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdbd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdbd9-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdbd9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdbd9-105">DESCRIPTION</span></span>
<span data-ttu-id="fdbd9-106">Cmdleten **New-AzureRmContainerServiceConfig** skapar ett lokalt konfigurations objekt för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="fdbd9-107">Skapa en behållar tjänst genom att lägga till det här objektet i New-AzureRmContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="fdbd9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdbd9-108">EXAMPLES</span></span>

### <span data-ttu-id="fdbd9-109">Exempel 1: skapa en konfiguration för en container tjänst</span><span class="sxs-lookup"><span data-stu-id="fdbd9-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="fdbd9-110">Det här kommandot skapar en container och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="fdbd9-111">Kommandot anger olika inställningar för behållar tjänst konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="fdbd9-112">Kommandot skickar konfigurationsobjektet till Add-AzureRmContainerServiceAgentPoolProfile cmdlet genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="fdbd9-113">Denna cmdlet lägger till en cacheprofil för poolen.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="fdbd9-114">Ange ett objekt i $Container för parametern *ContainerService* för **New-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="fdbd9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdbd9-115">PARAMETERS</span></span>

### <span data-ttu-id="fdbd9-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="fdbd9-116">-AdminUsername</span></span>
<span data-ttu-id="fdbd9-117">Anger det administratörs konto namn som ska användas för en Linux-baserad behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="fdbd9-118">-AgentPoolProfile</span></span>
<span data-ttu-id="fdbd9-119">Anger en matris för programpoolens profil objekt för behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="fdbd9-120">Lägga till en profil med hjälp av Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="fdbd9-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="fdbd9-122">Anger Orchestrator för anpassad profil.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdbd9-123">-DefaultProfile</span></span>
<span data-ttu-id="fdbd9-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdbd9-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="fdbd9-125">-Location</span></span>
<span data-ttu-id="fdbd9-126">Anger den plats där behållar tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="fdbd9-127">-MasterCount</span></span>
<span data-ttu-id="fdbd9-128">Anger hur många huvud datorer som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="fdbd9-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="fdbd9-130">Anger DNS-prefix för den virtuella huvud datorn.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="fdbd9-131">-OrchestratorType</span></span>
<span data-ttu-id="fdbd9-132">Anger typen av Orchestrator för behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="fdbd9-133">De acceptabla värdena för den här parametern är: DCOS och Swarm.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="fdbd9-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="fdbd9-135">Anger klient-ID för huvud profil.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="fdbd9-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="fdbd9-137">Anger huvud profil hemligheten.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="fdbd9-138">-SshPublicKey</span></span>
<span data-ttu-id="fdbd9-139">Anger den offentliga SSH-tangenten för en Linux-baserad behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fdbd9-140">-Tag</span></span>
<span data-ttu-id="fdbd9-141">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fdbd9-142">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="fdbd9-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="fdbd9-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="fdbd9-144">Anger om den här konfigurationen aktiverar diagnostik för behållar tjänstens virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="fdbd9-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="fdbd9-146">Anger administratörs lösen ordet för en behållar tjänst som använder operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="fdbd9-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="fdbd9-148">Anger administratörs namnet för en behållar tjänst som använder operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd9-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fdbd9-149">-Confirm</span></span>
<span data-ttu-id="fdbd9-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdbd9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdbd9-151">-WhatIf</span></span>
<span data-ttu-id="fdbd9-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdbd9-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdbd9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbd9-154">CommonParameters</span></span>
<span data-ttu-id="fdbd9-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdbd9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbd9-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdbd9-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbd9-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdbd9-157">INPUTS</span></span>

### <span data-ttu-id="fdbd9-158">System. String</span><span class="sxs-lookup"><span data-stu-id="fdbd9-158">System.String</span></span>

### <span data-ttu-id="fdbd9-159">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="fdbd9-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fdbd9-160">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. Compute, version = 21.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fdbd9-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fdbd9-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fdbd9-161">System.Int32</span></span>

### <span data-ttu-id="fdbd9-162">Microsoft. Azure. Management. Compute. Models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="fdbd9-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="fdbd9-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="fdbd9-163">System.String[]</span></span>

### <span data-ttu-id="fdbd9-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdbd9-164">System.Boolean</span></span>

## <span data-ttu-id="fdbd9-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdbd9-165">OUTPUTS</span></span>

### <span data-ttu-id="fdbd9-166">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="fdbd9-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="fdbd9-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdbd9-167">NOTES</span></span>

## <span data-ttu-id="fdbd9-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdbd9-168">RELATED LINKS</span></span>

[<span data-ttu-id="fdbd9-169">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="fdbd9-169">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="fdbd9-170">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fdbd9-170">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)
