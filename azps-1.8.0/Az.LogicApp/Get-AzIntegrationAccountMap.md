---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 39e78dfc27c325b9327d8ca7c27d800d656e3536
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916089"
---
# <span data-ttu-id="257fe-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257fe-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="257fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="257fe-102">SYNOPSIS</span></span>
<span data-ttu-id="257fe-103">Hämtar en översikt över integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="257fe-103">Gets an integration account map.</span></span>

## <span data-ttu-id="257fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="257fe-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="257fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="257fe-105">DESCRIPTION</span></span>
<span data-ttu-id="257fe-106">Cmdleten **Get-AzIntegrationAccountMap** tar en integrerings konto mappning från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="257fe-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="257fe-107">Ange integrerings konto namn, resurs grupps namn och kart namn.</span><span class="sxs-lookup"><span data-stu-id="257fe-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="257fe-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="257fe-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="257fe-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="257fe-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="257fe-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="257fe-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="257fe-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="257fe-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="257fe-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="257fe-112">EXAMPLES</span></span>

### <span data-ttu-id="257fe-113">Exempel 1: Hämta en integrerings konto karta</span><span class="sxs-lookup"><span data-stu-id="257fe-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="257fe-114">Det här kommandot får en integrerings konto översikt med namnet IntegrationAccountMap47 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="257fe-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="257fe-115">Exempel 2: Hämta integrerings konto mappningar utifrån integrerings konto namn</span><span class="sxs-lookup"><span data-stu-id="257fe-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="257fe-116">Det här kommandot får integrerings konto översikter med namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="257fe-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="257fe-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="257fe-117">PARAMETERS</span></span>

### <span data-ttu-id="257fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257fe-118">-DefaultProfile</span></span>
<span data-ttu-id="257fe-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="257fe-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="257fe-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="257fe-120">-MapName</span></span>
<span data-ttu-id="257fe-121">Anger namnet på en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="257fe-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="257fe-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="257fe-122">-Name</span></span>
<span data-ttu-id="257fe-123">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="257fe-123">Specifies the name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="257fe-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="257fe-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="257fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257fe-126">CommonParameters</span></span>
<span data-ttu-id="257fe-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257fe-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257fe-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257fe-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="257fe-129">INPUTS</span></span>

### <span data-ttu-id="257fe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="257fe-130">System.String</span></span>

## <span data-ttu-id="257fe-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="257fe-131">OUTPUTS</span></span>

### <span data-ttu-id="257fe-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257fe-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="257fe-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="257fe-133">NOTES</span></span>

## <span data-ttu-id="257fe-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="257fe-134">RELATED LINKS</span></span>

[<span data-ttu-id="257fe-135">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257fe-135">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="257fe-136">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257fe-136">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="257fe-137">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="257fe-137">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


