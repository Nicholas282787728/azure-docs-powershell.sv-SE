---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092070"
---
# <span data-ttu-id="96c6c-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="96c6c-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="96c6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="96c6c-103">Hämtar en URL för en logik program utlösare.</span><span class="sxs-lookup"><span data-stu-id="96c6c-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="96c6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96c6c-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c6c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="96c6c-106">Cmdleten **Get-AzLogicAppTriggerCallbackUrl** hämtar en URL-adress för en logik program utlösare från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="96c6c-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="96c6c-107">Denna cmdlet returnerar ett **WorkflowTriggerCallbackUrl** -objekt som representerar URL-adressen för återuppringning.</span><span class="sxs-lookup"><span data-stu-id="96c6c-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="96c6c-108">Ange namnet på resurs gruppen, namnet på logik programmet och Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="96c6c-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="96c6c-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="96c6c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="96c6c-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="96c6c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="96c6c-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="96c6c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="96c6c-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="96c6c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="96c6c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96c6c-113">EXAMPLES</span></span>

### <span data-ttu-id="96c6c-114">Exempel 1: Hämta en URL för en logik program utlösare</span><span class="sxs-lookup"><span data-stu-id="96c6c-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="96c6c-115">Det här kommandot får en URL för en logik program utlösare.</span><span class="sxs-lookup"><span data-stu-id="96c6c-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="96c6c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96c6c-116">PARAMETERS</span></span>

### <span data-ttu-id="96c6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c6c-117">-DefaultProfile</span></span>
<span data-ttu-id="96c6c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="96c6c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96c6c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="96c6c-119">-Name</span></span>
<span data-ttu-id="96c6c-120">Anger namnet på en logik-app.</span><span class="sxs-lookup"><span data-stu-id="96c6c-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="96c6c-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="96c6c-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c6c-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="96c6c-123">-TriggerName</span></span>
<span data-ttu-id="96c6c-124">Anger namnet på en utlösare.</span><span class="sxs-lookup"><span data-stu-id="96c6c-124">Specifies the name of a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c6c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c6c-125">CommonParameters</span></span>
<span data-ttu-id="96c6c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c6c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c6c-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c6c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c6c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96c6c-128">INPUTS</span></span>

### <span data-ttu-id="96c6c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="96c6c-129">System.String</span></span>

## <span data-ttu-id="96c6c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96c6c-130">OUTPUTS</span></span>

### <span data-ttu-id="96c6c-131">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="96c6c-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="96c6c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96c6c-132">NOTES</span></span>

## <span data-ttu-id="96c6c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96c6c-133">RELATED LINKS</span></span>

[<span data-ttu-id="96c6c-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="96c6c-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


