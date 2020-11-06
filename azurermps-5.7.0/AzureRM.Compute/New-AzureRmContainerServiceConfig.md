---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 0568359131a91beeb175d69da51d1646bd28f88e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573537"
---
# <span data-ttu-id="e746d-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="e746d-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="e746d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e746d-102">SYNOPSIS</span></span>
<span data-ttu-id="e746d-103">Skapar ett lokalt konfigurations objekt för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="e746d-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e746d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e746d-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e746d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e746d-105">DESCRIPTION</span></span>
<span data-ttu-id="e746d-106">Cmdleten **New-AzureRmContainerServiceConfig** skapar ett lokalt konfigurations objekt för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="e746d-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="e746d-107">Skapa en behållar tjänst genom att lägga till det här objektet i New-AzureRmContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e746d-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="e746d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e746d-108">EXAMPLES</span></span>

### <span data-ttu-id="e746d-109">Exempel 1: skapa en konfiguration för en container tjänst</span><span class="sxs-lookup"><span data-stu-id="e746d-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="e746d-110">Det här kommandot skapar en container och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="e746d-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="e746d-111">Kommandot anger olika inställningar för behållar tjänst konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e746d-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="e746d-112">Kommandot skickar konfigurationsobjektet till Add-AzureRmContainerServiceAgentPoolProfile cmdlet genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e746d-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e746d-113">Denna cmdlet lägger till en cacheprofil för poolen.</span><span class="sxs-lookup"><span data-stu-id="e746d-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="e746d-114">Ange ett objekt i $Container för parametern *ContainerService* för **New-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="e746d-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="e746d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e746d-115">PARAMETERS</span></span>

### <span data-ttu-id="e746d-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="e746d-116">-AdminUsername</span></span>
<span data-ttu-id="e746d-117">Anger det administratörs konto namn som ska användas för en Linux-baserad behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="e746d-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e746d-118">-AgentPoolProfile</span></span>
<span data-ttu-id="e746d-119">Anger en matris för programpoolens profil objekt för behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e746d-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="e746d-120">Lägga till en profil med hjälp av Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e746d-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="e746d-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="e746d-122">Anger Orchestrator för anpassad profil.</span><span class="sxs-lookup"><span data-stu-id="e746d-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="e746d-123">-Location</span></span>
<span data-ttu-id="e746d-124">Anger den plats där behållar tjänsten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e746d-124">Specifies the location in which to create the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-125">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="e746d-125">-MasterCount</span></span>
<span data-ttu-id="e746d-126">Anger hur många huvud datorer som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e746d-126">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-127">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="e746d-127">-MasterDnsPrefix</span></span>
<span data-ttu-id="e746d-128">Anger DNS-prefix för den virtuella huvud datorn.</span><span class="sxs-lookup"><span data-stu-id="e746d-128">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-129">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="e746d-129">-OrchestratorType</span></span>
<span data-ttu-id="e746d-130">Anger typen av Orchestrator för behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e746d-130">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="e746d-131">De acceptabla värdena för den här parametern är: DCOS och Swarm.</span><span class="sxs-lookup"><span data-stu-id="e746d-131">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: ContainerServiceOrchestratorTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-132">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="e746d-132">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="e746d-133">Anger klient-ID för huvud profil.</span><span class="sxs-lookup"><span data-stu-id="e746d-133">Specifies the principal profile client ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-134">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="e746d-134">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="e746d-135">Anger huvud profil hemligheten.</span><span class="sxs-lookup"><span data-stu-id="e746d-135">Specifies the principal profile secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-136">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e746d-136">-SshPublicKey</span></span>
<span data-ttu-id="e746d-137">Anger den offentliga SSH-tangenten för en Linux-baserad behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="e746d-137">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e746d-138">-Tag</span></span>
<span data-ttu-id="e746d-139">Anger taggar för behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e746d-139">Specifies tags for the container service.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-140">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="e746d-140">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="e746d-141">Anger om den här konfigurationen aktiverar diagnostik för behållar tjänstens virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="e746d-141">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-142">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="e746d-142">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="e746d-143">Anger administratörs lösen ordet för en behållar tjänst som använder operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="e746d-143">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-144">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="e746d-144">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="e746d-145">Anger administratörs namnet för en behållar tjänst som använder operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="e746d-145">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e746d-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e746d-146">-Confirm</span></span>
<span data-ttu-id="e746d-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e746d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e746d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e746d-148">-WhatIf</span></span>
<span data-ttu-id="e746d-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e746d-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e746d-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e746d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e746d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e746d-151">CommonParameters</span></span>
<span data-ttu-id="e746d-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e746d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e746d-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e746d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e746d-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e746d-154">INPUTS</span></span>

### <span data-ttu-id="e746d-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="e746d-155">None</span></span>
<span data-ttu-id="e746d-156">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e746d-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e746d-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e746d-157">OUTPUTS</span></span>

## <span data-ttu-id="e746d-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e746d-158">NOTES</span></span>

## <span data-ttu-id="e746d-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e746d-159">RELATED LINKS</span></span>

[<span data-ttu-id="e746d-160">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e746d-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="e746d-161">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="e746d-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


