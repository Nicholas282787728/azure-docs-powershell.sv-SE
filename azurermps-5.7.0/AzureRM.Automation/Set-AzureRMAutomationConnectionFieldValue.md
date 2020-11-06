---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: 84da08588838982353bc8c39354452bec1a17a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582135"
---
# <span data-ttu-id="0fa36-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="0fa36-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="0fa36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fa36-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa36-103">Ändrar värdet för ett fält i en Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="0fa36-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fa36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fa36-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fa36-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fa36-105">DESCRIPTION</span></span>
<span data-ttu-id="0fa36-106">Cmdleten **set-AzureRmAutomationConnectionFieldValue** ändrar värdet för ett fält i en anslutning i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0fa36-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="0fa36-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fa36-107">EXAMPLES</span></span>

### <span data-ttu-id="0fa36-108">Exempel 1: ändra ett fält värde i en anslutning</span><span class="sxs-lookup"><span data-stu-id="0fa36-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="0fa36-109">Det här kommandot ändrar prenumerations-ID för Azure-anslutningen som heter ContosoConnection i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="0fa36-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="0fa36-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fa36-110">PARAMETERS</span></span>

### <span data-ttu-id="0fa36-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0fa36-111">-AutomationAccountName</span></span>
<span data-ttu-id="0fa36-112">Anger namnet på det Automation-konto som denna cmdlet ändrar ett fält i en anslutning till.</span><span class="sxs-lookup"><span data-stu-id="0fa36-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa36-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="0fa36-113">-ConnectionFieldName</span></span>
<span data-ttu-id="0fa36-114">Anger ett namn för fältet som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0fa36-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa36-115">-DefaultProfile</span></span>
<span data-ttu-id="0fa36-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0fa36-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fa36-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fa36-117">-Name</span></span>
<span data-ttu-id="0fa36-118">Anger ett namn för den anslutning där denna cmdlet ändrar ett fält.</span><span class="sxs-lookup"><span data-stu-id="0fa36-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa36-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa36-119">-ResourceGroupName</span></span>
<span data-ttu-id="0fa36-120">Anger namnet på den resurs grupp för vilken denna cmdlet ändrar ett fält i en anslutning.</span><span class="sxs-lookup"><span data-stu-id="0fa36-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa36-121">-Värde</span><span class="sxs-lookup"><span data-stu-id="0fa36-121">-Value</span></span>
<span data-ttu-id="0fa36-122">Anger det värde som ska ändras i fältet Connection.</span><span class="sxs-lookup"><span data-stu-id="0fa36-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa36-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa36-123">CommonParameters</span></span>
<span data-ttu-id="0fa36-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa36-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa36-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa36-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa36-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fa36-126">INPUTS</span></span>

### <span data-ttu-id="0fa36-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="0fa36-127">None</span></span>
<span data-ttu-id="0fa36-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0fa36-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0fa36-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fa36-129">OUTPUTS</span></span>

### <span data-ttu-id="0fa36-130">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="0fa36-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="0fa36-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fa36-131">NOTES</span></span>

## <span data-ttu-id="0fa36-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fa36-132">RELATED LINKS</span></span>

[<span data-ttu-id="0fa36-133">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0fa36-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


