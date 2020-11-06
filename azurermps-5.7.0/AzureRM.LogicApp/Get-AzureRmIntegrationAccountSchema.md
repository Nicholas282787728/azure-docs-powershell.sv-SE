---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 8ad8714a59ac9f0beb0c070d5f9f89c4fbd20a43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581131"
---
# <span data-ttu-id="cefd8-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cefd8-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="cefd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cefd8-102">SYNOPSIS</span></span>
<span data-ttu-id="cefd8-103">Hämtar schema för integrerings konton.</span><span class="sxs-lookup"><span data-stu-id="cefd8-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cefd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cefd8-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cefd8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cefd8-105">DESCRIPTION</span></span>
<span data-ttu-id="cefd8-106">Cmdleten **Get-AzureRmIntegrationAccountSchema** hämtar ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="cefd8-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="cefd8-107">Ange integrerings konto namn, resurs grupps namn och schema namn.</span><span class="sxs-lookup"><span data-stu-id="cefd8-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="cefd8-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="cefd8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cefd8-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="cefd8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cefd8-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="cefd8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cefd8-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="cefd8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cefd8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cefd8-112">EXAMPLES</span></span>

### <span data-ttu-id="cefd8-113">Exempel 1: skaffa ett integrations konto schema</span><span class="sxs-lookup"><span data-stu-id="cefd8-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
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

<span data-ttu-id="cefd8-114">Det här kommandot får integrerings kontots schema med namnet IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="cefd8-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="cefd8-115">Exempel 2: skaffa ett integrations konto schema för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="cefd8-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="cefd8-116">Det här kommandot får integrerings konto scheman för resurs gruppen "ResourceGroup11".</span><span class="sxs-lookup"><span data-stu-id="cefd8-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="cefd8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cefd8-117">PARAMETERS</span></span>

### <span data-ttu-id="cefd8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefd8-118">-DefaultProfile</span></span>
<span data-ttu-id="cefd8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cefd8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cefd8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cefd8-120">-Name</span></span>
<span data-ttu-id="cefd8-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="cefd8-121">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cefd8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cefd8-122">-ResourceGroupName</span></span>
<span data-ttu-id="cefd8-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cefd8-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cefd8-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cefd8-124">-SchemaName</span></span>
<span data-ttu-id="cefd8-125">Anger namnet på ett integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="cefd8-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="cefd8-126">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="cefd8-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="cefd8-127">.</span><span class="sxs-lookup"><span data-stu-id="cefd8-127">.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cefd8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefd8-128">CommonParameters</span></span>
<span data-ttu-id="cefd8-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cefd8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefd8-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cefd8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefd8-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cefd8-131">INPUTS</span></span>

### <span data-ttu-id="cefd8-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="cefd8-132">None</span></span>
<span data-ttu-id="cefd8-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cefd8-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cefd8-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cefd8-134">OUTPUTS</span></span>

### <span data-ttu-id="cefd8-135">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cefd8-135">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="cefd8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cefd8-136">NOTES</span></span>

## <span data-ttu-id="cefd8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cefd8-137">RELATED LINKS</span></span>

[<span data-ttu-id="cefd8-138">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cefd8-138">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="cefd8-139">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cefd8-139">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="cefd8-140">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cefd8-140">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


