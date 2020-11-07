---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: ad4954a8344fd34e881c9bae75d6ba31f9d099a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743802"
---
# <span data-ttu-id="f3911-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3911-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="f3911-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3911-102">SYNOPSIS</span></span>
<span data-ttu-id="f3911-103">Hämtar en översikt över integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="f3911-103">Gets an integration account map.</span></span>

## <span data-ttu-id="f3911-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3911-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3911-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3911-105">DESCRIPTION</span></span>
<span data-ttu-id="f3911-106">Cmdleten **Get-AzIntegrationAccountMap** tar en integrerings konto mappning från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f3911-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="f3911-107">Ange integrerings konto namn, resurs grupps namn och kart namn.</span><span class="sxs-lookup"><span data-stu-id="f3911-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="f3911-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="f3911-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f3911-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="f3911-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f3911-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f3911-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f3911-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="f3911-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f3911-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3911-112">EXAMPLES</span></span>

### <span data-ttu-id="f3911-113">Exempel 1: Hämta en integrerings konto karta</span><span class="sxs-lookup"><span data-stu-id="f3911-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="f3911-114">Det här kommandot får en integrerings konto översikt med namnet IntegrationAccountMap47 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f3911-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="f3911-115">Exempel 2: Hämta integrerings konto mappningar utifrån integrerings konto namn</span><span class="sxs-lookup"><span data-stu-id="f3911-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="f3911-116">Det här kommandot får integrerings konto översikter med namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="f3911-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="f3911-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3911-117">PARAMETERS</span></span>

### <span data-ttu-id="f3911-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3911-118">-DefaultProfile</span></span>
<span data-ttu-id="f3911-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f3911-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3911-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="f3911-120">-MapName</span></span>
<span data-ttu-id="f3911-121">Anger namnet på en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="f3911-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="f3911-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="f3911-122">-MapType</span></span>
<span data-ttu-id="f3911-123">Typ av integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="f3911-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3911-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3911-124">-Name</span></span>
<span data-ttu-id="f3911-125">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="f3911-125">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="f3911-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3911-126">-ResourceGroupName</span></span>
<span data-ttu-id="f3911-127">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f3911-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f3911-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3911-128">CommonParameters</span></span>
<span data-ttu-id="f3911-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3911-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3911-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3911-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3911-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3911-131">INPUTS</span></span>

### <span data-ttu-id="f3911-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f3911-132">System.String</span></span>

## <span data-ttu-id="f3911-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3911-133">OUTPUTS</span></span>

### <span data-ttu-id="f3911-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3911-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="f3911-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3911-135">NOTES</span></span>

## <span data-ttu-id="f3911-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3911-136">RELATED LINKS</span></span>

[<span data-ttu-id="f3911-137">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3911-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="f3911-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3911-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="f3911-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f3911-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)

