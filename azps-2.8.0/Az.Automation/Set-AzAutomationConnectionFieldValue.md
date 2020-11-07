---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 71f044dcce4944960d10fe2946b48c04354b8256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745469"
---
# <span data-ttu-id="eb7ca-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="eb7ca-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="eb7ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7ca-103">Ändrar värdet för ett fält i en Automation-anslutning.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="eb7ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb7ca-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb7ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb7ca-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7ca-106">Cmdleten **set-AzAutomationConnectionFieldValue** ändrar värdet för ett fält i en anslutning i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="eb7ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb7ca-107">EXAMPLES</span></span>

### <span data-ttu-id="eb7ca-108">Exempel 1: ändra ett fält värde i en anslutning</span><span class="sxs-lookup"><span data-stu-id="eb7ca-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="eb7ca-109">Det här kommandot ändrar prenumerations-ID för Azure-anslutningen som heter ContosoConnection i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="eb7ca-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb7ca-110">PARAMETERS</span></span>

### <span data-ttu-id="eb7ca-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eb7ca-111">-AutomationAccountName</span></span>
<span data-ttu-id="eb7ca-112">Anger namnet på det Automation-konto som denna cmdlet ändrar ett fält i en anslutning till.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ca-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="eb7ca-113">-ConnectionFieldName</span></span>
<span data-ttu-id="eb7ca-114">Anger ett namn för fältet som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eb7ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7ca-115">-DefaultProfile</span></span>
<span data-ttu-id="eb7ca-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="eb7ca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb7ca-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb7ca-117">-Name</span></span>
<span data-ttu-id="eb7ca-118">Anger ett namn för den anslutning där denna cmdlet ändrar ett fält.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb7ca-120">Anger namnet på den resurs grupp för vilken denna cmdlet ändrar ett fält i en anslutning.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ca-121">-Värde</span><span class="sxs-lookup"><span data-stu-id="eb7ca-121">-Value</span></span>
<span data-ttu-id="eb7ca-122">Anger det värde som ska ändras i fältet Connection.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7ca-123">CommonParameters</span></span>
<span data-ttu-id="eb7ca-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7ca-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7ca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7ca-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb7ca-126">INPUTS</span></span>

### <span data-ttu-id="eb7ca-127">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7ca-127">System.String</span></span>

### <span data-ttu-id="eb7ca-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="eb7ca-128">System.Object</span></span>

## <span data-ttu-id="eb7ca-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb7ca-129">OUTPUTS</span></span>

### <span data-ttu-id="eb7ca-130">Microsoft. Azure. commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="eb7ca-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="eb7ca-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb7ca-131">NOTES</span></span>

## <span data-ttu-id="eb7ca-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb7ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="eb7ca-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="eb7ca-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


