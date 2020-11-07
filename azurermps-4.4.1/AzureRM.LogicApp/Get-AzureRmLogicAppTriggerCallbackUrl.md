---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: f9ac8c7d7131b53b04e7da03eeb17aea33507258
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582384"
---
# <span data-ttu-id="d032b-101">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d032b-101">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="d032b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d032b-102">SYNOPSIS</span></span>
<span data-ttu-id="d032b-103">Hämtar en URL för en logik program utlösare.</span><span class="sxs-lookup"><span data-stu-id="d032b-103">Gets a Logic App trigger callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d032b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d032b-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d032b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d032b-105">DESCRIPTION</span></span>
<span data-ttu-id="d032b-106">Cmdleten **Get-AzureRmLogicAppTriggerCallbackUrl** hämtar en URL-adress för en logik program utlösare från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d032b-106">The **Get-AzureRmLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="d032b-107">Denna cmdlet returnerar ett **WorkflowTriggerCallbackUrl** -objekt som representerar URL-adressen för återuppringning.</span><span class="sxs-lookup"><span data-stu-id="d032b-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="d032b-108">Ange namnet på resurs gruppen, namnet på logik programmet och Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="d032b-108">Specify the resource group name, logic app name, and trigger name.</span></span>

<span data-ttu-id="d032b-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="d032b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d032b-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="d032b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d032b-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="d032b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d032b-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="d032b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d032b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d032b-113">EXAMPLES</span></span>

### <span data-ttu-id="d032b-114">Exempel 1: Hämta en URL för en logik program utlösare</span><span class="sxs-lookup"><span data-stu-id="d032b-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="d032b-115">Det här kommandot får en URL för en logik program utlösare.</span><span class="sxs-lookup"><span data-stu-id="d032b-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="d032b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d032b-116">PARAMETERS</span></span>

### <span data-ttu-id="d032b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d032b-117">-Name</span></span>
<span data-ttu-id="d032b-118">Anger namnet på en logik-app.</span><span class="sxs-lookup"><span data-stu-id="d032b-118">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="d032b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d032b-119">-ResourceGroupName</span></span>
<span data-ttu-id="d032b-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d032b-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d032b-121">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="d032b-121">-TriggerName</span></span>
<span data-ttu-id="d032b-122">Anger namnet på en utlösare.</span><span class="sxs-lookup"><span data-stu-id="d032b-122">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="d032b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d032b-123">-DefaultProfile</span></span>
<span data-ttu-id="d032b-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d032b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d032b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d032b-125">CommonParameters</span></span>
<span data-ttu-id="d032b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d032b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d032b-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d032b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d032b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d032b-128">INPUTS</span></span>

## <span data-ttu-id="d032b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d032b-129">OUTPUTS</span></span>

### <span data-ttu-id="d032b-130">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d032b-130">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="d032b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d032b-131">NOTES</span></span>

## <span data-ttu-id="d032b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d032b-132">RELATED LINKS</span></span>

[<span data-ttu-id="d032b-133">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d032b-133">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

