---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: 5631ab93c4c9d0fd89b56043d32bc685b042ace9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745115"
---
# <span data-ttu-id="59732-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="59732-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="59732-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59732-102">SYNOPSIS</span></span>
<span data-ttu-id="59732-103">Skapar ett lokalt konfigurations objekt för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="59732-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="59732-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59732-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59732-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59732-105">DESCRIPTION</span></span>
<span data-ttu-id="59732-106">Cmdleten **New-AzContainerServiceConfig** skapar ett lokalt konfigurations objekt för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="59732-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="59732-107">Skapa en behållar tjänst genom att lägga till det här objektet i New-AzContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59732-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="59732-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59732-108">EXAMPLES</span></span>

### <span data-ttu-id="59732-109">Exempel 1: skapa en konfiguration för en container tjänst</span><span class="sxs-lookup"><span data-stu-id="59732-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="59732-110">Det här kommandot skapar en container och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="59732-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="59732-111">Kommandot anger olika inställningar för behållar tjänst konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="59732-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="59732-112">Kommandot skickar konfigurationsobjektet till Add-AzContainerServiceAgentPoolProfile cmdlet genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="59732-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="59732-113">Denna cmdlet lägger till en cacheprofil för poolen.</span><span class="sxs-lookup"><span data-stu-id="59732-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="59732-114">Ange ett objekt i $Container för parametern *ContainerService* för **New-AzContainerService**.</span><span class="sxs-lookup"><span data-stu-id="59732-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="59732-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59732-115">PARAMETERS</span></span>

### <span data-ttu-id="59732-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="59732-116">-AdminUsername</span></span>
<span data-ttu-id="59732-117">Anger det administratörs konto namn som ska användas för en Linux-baserad behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="59732-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="59732-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="59732-118">-AgentPoolProfile</span></span>
<span data-ttu-id="59732-119">Anger en matris för programpoolens profil objekt för behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="59732-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="59732-120">Lägga till en profil med hjälp av Add-AzContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59732-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="59732-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="59732-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="59732-122">Anger Orchestrator för anpassad profil.</span><span class="sxs-lookup"><span data-stu-id="59732-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="59732-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59732-123">-DefaultProfile</span></span>
<span data-ttu-id="59732-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59732-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59732-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="59732-125">-Location</span></span>
<span data-ttu-id="59732-126">Anger den plats där behållar tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="59732-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="59732-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="59732-127">-MasterCount</span></span>
<span data-ttu-id="59732-128">Anger hur många huvud datorer som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="59732-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="59732-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="59732-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="59732-130">Anger DNS-prefix för den virtuella huvud datorn.</span><span class="sxs-lookup"><span data-stu-id="59732-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="59732-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="59732-131">-OrchestratorType</span></span>
<span data-ttu-id="59732-132">Anger typen av Orchestrator för behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="59732-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="59732-133">De acceptabla värdena för den här parametern är: DCOS och Swarm.</span><span class="sxs-lookup"><span data-stu-id="59732-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="59732-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="59732-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="59732-135">Anger klient-ID för huvud profil.</span><span class="sxs-lookup"><span data-stu-id="59732-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="59732-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="59732-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="59732-137">Anger huvud profil hemligheten.</span><span class="sxs-lookup"><span data-stu-id="59732-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="59732-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="59732-138">-SshPublicKey</span></span>
<span data-ttu-id="59732-139">Anger den offentliga SSH-tangenten för en Linux-baserad behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="59732-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="59732-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="59732-140">-Tag</span></span>
<span data-ttu-id="59732-141">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="59732-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59732-142">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="59732-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59732-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="59732-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="59732-144">Anger om den här konfigurationen aktiverar diagnostik för behållar tjänstens virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="59732-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="59732-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="59732-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="59732-146">Anger administratörs lösen ordet för en behållar tjänst som använder operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="59732-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="59732-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="59732-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="59732-148">Anger administratörs namnet för en behållar tjänst som använder operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="59732-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="59732-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59732-149">-Confirm</span></span>
<span data-ttu-id="59732-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59732-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59732-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59732-151">-WhatIf</span></span>
<span data-ttu-id="59732-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59732-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59732-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59732-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59732-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59732-154">CommonParameters</span></span>
<span data-ttu-id="59732-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59732-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59732-156">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59732-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59732-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59732-157">INPUTS</span></span>

### <span data-ttu-id="59732-158">System. String</span><span class="sxs-lookup"><span data-stu-id="59732-158">System.String</span></span>

### <span data-ttu-id="59732-159">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="59732-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="59732-160">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="59732-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="59732-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="59732-161">System.Int32</span></span>

### <span data-ttu-id="59732-162">Microsoft. Azure. Management. Compute. Models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="59732-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="59732-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="59732-163">System.String[]</span></span>

### <span data-ttu-id="59732-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59732-164">System.Boolean</span></span>

## <span data-ttu-id="59732-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59732-165">OUTPUTS</span></span>

### <span data-ttu-id="59732-166">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="59732-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="59732-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59732-167">NOTES</span></span>

## <span data-ttu-id="59732-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59732-168">RELATED LINKS</span></span>

[<span data-ttu-id="59732-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="59732-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="59732-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="59732-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
