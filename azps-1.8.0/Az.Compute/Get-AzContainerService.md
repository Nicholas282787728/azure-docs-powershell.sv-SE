---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 9d8afa31d296e62c75b869bd93e6f96aadf82328
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754591"
---
# <span data-ttu-id="e1579-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e1579-101">Get-AzContainerService</span></span>

## <span data-ttu-id="e1579-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1579-102">SYNOPSIS</span></span>
<span data-ttu-id="e1579-103">Hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="e1579-103">Gets a container service.</span></span>

## <span data-ttu-id="e1579-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1579-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1579-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1579-105">DESCRIPTION</span></span>
<span data-ttu-id="e1579-106">Cmdleten **Get-AzContainerService** hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="e1579-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="e1579-107">Du kan visa egenskaperna för en behållar tjänst, vilket inkluderar tillstånd, antalet huvud och agenter samt det fullt kvalificerade domän namnet för huvud gruppen och agenten.</span><span class="sxs-lookup"><span data-stu-id="e1579-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="e1579-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1579-108">EXAMPLES</span></span>

### <span data-ttu-id="e1579-109">Exempel 1: skaffa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="e1579-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="e1579-110">Det här kommandot får en behållar tjänst som heter CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="e1579-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="e1579-111">Exempel 2: Hämta alla behållar tjänster</span><span class="sxs-lookup"><span data-stu-id="e1579-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="e1579-112">Det här kommandot får alla behållar tjänster i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e1579-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="e1579-113">Exempel 3: Hämta alla behållar tjänster i resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e1579-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="e1579-114">Det här kommandot får alla behållar tjänster i ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="e1579-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="e1579-115">Exempel 4: Hämta alla behållar tjänster med filter</span><span class="sxs-lookup"><span data-stu-id="e1579-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="e1579-116">Det här kommandot får alla behållar tjänster som börjar med "CSResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="e1579-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="e1579-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1579-117">PARAMETERS</span></span>

### <span data-ttu-id="e1579-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1579-118">-DefaultProfile</span></span>
<span data-ttu-id="e1579-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1579-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1579-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1579-120">-Name</span></span>
<span data-ttu-id="e1579-121">Anger namnet på den behållar tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="e1579-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e1579-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1579-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1579-123">Anger resurs gruppen för den behållar tjänst som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="e1579-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e1579-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1579-124">CommonParameters</span></span>
<span data-ttu-id="e1579-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1579-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1579-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1579-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1579-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1579-127">INPUTS</span></span>

### <span data-ttu-id="e1579-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e1579-128">System.String</span></span>

## <span data-ttu-id="e1579-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1579-129">OUTPUTS</span></span>

### <span data-ttu-id="e1579-130">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e1579-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e1579-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1579-131">NOTES</span></span>

## <span data-ttu-id="e1579-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1579-132">RELATED LINKS</span></span>

[<span data-ttu-id="e1579-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e1579-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="e1579-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e1579-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="e1579-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e1579-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


