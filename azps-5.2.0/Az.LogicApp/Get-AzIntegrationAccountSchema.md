---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416128"
---
# <span data-ttu-id="13750-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="13750-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="13750-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13750-102">SYNOPSIS</span></span>
<span data-ttu-id="13750-103">Hämtar schema för integrerings konton.</span><span class="sxs-lookup"><span data-stu-id="13750-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="13750-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13750-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13750-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13750-105">DESCRIPTION</span></span>
<span data-ttu-id="13750-106">Cmdleten **Get-AzIntegrationAccountSchema** hämtar ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="13750-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="13750-107">Ange integrerings konto namn, resurs grupps namn och schema namn.</span><span class="sxs-lookup"><span data-stu-id="13750-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="13750-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="13750-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="13750-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="13750-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="13750-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="13750-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="13750-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="13750-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="13750-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13750-112">EXAMPLES</span></span>

### <span data-ttu-id="13750-113">Exempel 1: skaffa ett integrations konto schema</span><span class="sxs-lookup"><span data-stu-id="13750-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="13750-114">Det här kommandot får integrerings kontots schema med namnet IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="13750-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="13750-115">Exempel 2: skaffa ett integrations konto schema för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="13750-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="13750-116">Det här kommandot får integrerings konto scheman för resurs gruppen "ResourceGroup11".</span><span class="sxs-lookup"><span data-stu-id="13750-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="13750-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13750-117">PARAMETERS</span></span>

### <span data-ttu-id="13750-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13750-118">-DefaultProfile</span></span>
<span data-ttu-id="13750-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="13750-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13750-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="13750-120">-Name</span></span>
<span data-ttu-id="13750-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="13750-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="13750-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13750-122">-ResourceGroupName</span></span>
<span data-ttu-id="13750-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="13750-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="13750-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="13750-124">-SchemaName</span></span>
<span data-ttu-id="13750-125">Anger namnet på ett integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="13750-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="13750-126">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="13750-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="13750-127">.</span><span class="sxs-lookup"><span data-stu-id="13750-127">.</span></span>

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

### <span data-ttu-id="13750-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13750-128">CommonParameters</span></span>
<span data-ttu-id="13750-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13750-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13750-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13750-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13750-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13750-131">INPUTS</span></span>

### <span data-ttu-id="13750-132">System. String</span><span class="sxs-lookup"><span data-stu-id="13750-132">System.String</span></span>

## <span data-ttu-id="13750-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13750-133">OUTPUTS</span></span>

### <span data-ttu-id="13750-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="13750-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="13750-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13750-135">NOTES</span></span>

## <span data-ttu-id="13750-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13750-136">RELATED LINKS</span></span>

[<span data-ttu-id="13750-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="13750-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="13750-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="13750-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="13750-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="13750-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


