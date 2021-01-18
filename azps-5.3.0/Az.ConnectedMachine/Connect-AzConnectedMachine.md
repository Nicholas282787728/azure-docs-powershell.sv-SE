---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524425"
---
# <span data-ttu-id="ac6ad-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="ac6ad-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="ac6ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac6ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6ad-103">API för att registrera en ny dator och därmed skapa en spårad resurs i armar</span><span class="sxs-lookup"><span data-stu-id="ac6ad-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="ac6ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac6ad-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="ac6ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac6ad-105">DESCRIPTION</span></span>
<span data-ttu-id="ac6ad-106">API för att registrera en ny dator och därmed skapa en spårad resurs i armar</span><span class="sxs-lookup"><span data-stu-id="ac6ad-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="ac6ad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac6ad-107">EXAMPLES</span></span>

### <span data-ttu-id="ac6ad-108">Exempel 1: informerar datorn om att du är ansluten till datorn</span><span class="sxs-lookup"><span data-stu-id="ac6ad-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="ac6ad-109">Informerar datorn om att du är ansluten till datorn.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="ac6ad-110">Exempel 2: inbyggda en fjärrdator som ansluten enhet</span><span class="sxs-lookup"><span data-stu-id="ac6ad-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="ac6ad-111">Hanterar en fjärrdator som en ansluten enhet med PowerShell-fjärrkommunikation.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="ac6ad-112">Obs! endast Windows som mål stöder just nu.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="ac6ad-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac6ad-113">PARAMETERS</span></span>

### <span data-ttu-id="ac6ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6ad-114">-DefaultProfile</span></span>
<span data-ttu-id="ac6ad-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6ad-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="ac6ad-116">-Location</span></span>
<span data-ttu-id="ac6ad-117">Platsen för den skapade ConnectedMachine.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-117">The location for the created ConnectedMachine.</span></span>

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

### <span data-ttu-id="ac6ad-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac6ad-118">-Name</span></span>
<span data-ttu-id="ac6ad-119">Det namn som ska användas för den här datorn.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="ac6ad-120">Värd namnet används som standard.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="ac6ad-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="ac6ad-121">-Proxy</span></span>
<span data-ttu-id="ac6ad-122">URI för proxyservern som ska användas</span><span class="sxs-lookup"><span data-stu-id="ac6ad-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6ad-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="ac6ad-123">-PSSession</span></span>
<span data-ttu-id="ac6ad-124">När det här alternativet anges körs kommandot som inbyggda maskiner till Azure i varje PSSession.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="ac6ad-125">Obs! det här fungerar bara i Windows för tillfället.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6ad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac6ad-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac6ad-127">Namnet på resurs gruppen där du vill lägga till datorn.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6ad-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac6ad-128">-SubscriptionId</span></span>
<span data-ttu-id="ac6ad-129">ID för den prenumeration där du vill lägga till datorn.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6ad-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ac6ad-130">-Tag</span></span>
<span data-ttu-id="ac6ad-131">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6ad-132">CommonParameters</span></span>
<span data-ttu-id="ac6ad-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac6ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6ad-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac6ad-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6ad-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac6ad-135">INPUTS</span></span>

## <span data-ttu-id="ac6ad-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac6ad-136">OUTPUTS</span></span>

## <span data-ttu-id="ac6ad-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac6ad-137">NOTES</span></span>

<span data-ttu-id="ac6ad-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ac6ad-138">ALIASES</span></span>

## <span data-ttu-id="ac6ad-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac6ad-139">RELATED LINKS</span></span>

