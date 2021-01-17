---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404403"
---
# <span data-ttu-id="ec5fb-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="ec5fb-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="ec5fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ec5fb-103">Test-AzStackHCIConnection verifiera anslutningar från lokala klustrade noder till de Azure-tjänster som krävs av Azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="ec5fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec5fb-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="ec5fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec5fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ec5fb-106">Test-AzStackHCIConnection verifiera anslutningar från lokala klustrade noder till de Azure-tjänster som krävs av Azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="ec5fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec5fb-107">EXAMPLES</span></span>

### <span data-ttu-id="ec5fb-108">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="ec5fb-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="ec5fb-109">C:\PS \> test-AzStackHCIConnection-test: Anslut till Azure Stack HCI-tjänsten EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: true result: lyckades</span><span class="sxs-lookup"><span data-stu-id="ec5fb-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="ec5fb-110">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="ec5fb-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="ec5fb-111">C:\PS \> test-AzStackHCIConnection test: Anslut till Azure Stack HCI-tjänsten EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: true result: misslyckad FailedNodes: Node1inClus2, Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="ec5fb-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="ec5fb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec5fb-112">PARAMETERS</span></span>

### <span data-ttu-id="ec5fb-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ec5fb-113">-ComputerName</span></span>
<span data-ttu-id="ec5fb-114">Anger en av klusternoderna i det lokala klustret som registreras på Azure.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="ec5fb-115">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="ec5fb-115">-Credential</span></span>
<span data-ttu-id="ec5fb-116">Anger autentiseringsuppgifter för dator namnet.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="ec5fb-117">Standard är den aktuella användaren som kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-117">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec5fb-118">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ec5fb-118">-EnvironmentName</span></span>
<span data-ttu-id="ec5fb-119">Anger Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="ec5fb-120">Standard är AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-120">Default is AzureCloud.</span></span>
<span data-ttu-id="ec5fb-121">Giltiga värden är AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="ec5fb-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec5fb-122">-Region</span><span class="sxs-lookup"><span data-stu-id="ec5fb-122">-Region</span></span>
<span data-ttu-id="ec5fb-123">Anger vilken region du vill ansluta till.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="ec5fb-124">Används inte såvida det inte är en Kanarie region.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-124">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="ec5fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec5fb-125">CommonParameters</span></span>
<span data-ttu-id="ec5fb-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec5fb-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec5fb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec5fb-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec5fb-128">INPUTS</span></span>

## <span data-ttu-id="ec5fb-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec5fb-129">OUTPUTS</span></span>

### <span data-ttu-id="ec5fb-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-130">PSCustomObject.</span></span> <span data-ttu-id="ec5fb-131">Returnerar följande egenskaper i PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="ec5fb-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="ec5fb-132">Test: namnet på testet som utförts.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="ec5fb-133">EndpointTested: slut punkt som används i testet.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="ec5fb-134">IsRequired: sant eller falskt</span><span class="sxs-lookup"><span data-stu-id="ec5fb-134">IsRequired: True or False</span></span>
### <span data-ttu-id="ec5fb-135">Resultat: lyckades eller misslyckades</span><span class="sxs-lookup"><span data-stu-id="ec5fb-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="ec5fb-136">FailedNodes: lista med noder där testet misslyckades.</span><span class="sxs-lookup"><span data-stu-id="ec5fb-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="ec5fb-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec5fb-137">NOTES</span></span>

## <span data-ttu-id="ec5fb-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec5fb-138">RELATED LINKS</span></span>
