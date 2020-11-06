---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 8bd043f11294b2290a5f54289232bc826c1f0d88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572971"
---
# <span data-ttu-id="fcfaf-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="fcfaf-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="fcfaf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfaf-103">Återskapar registrerings nycklar för ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="fcfaf-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcfaf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcfaf-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcfaf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcfaf-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfaf-106">Cmdleten **New-AzureRmAutomationKey** återskapar registrerings nycklar för ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="fcfaf-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="fcfaf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcfaf-107">EXAMPLES</span></span>

### <span data-ttu-id="fcfaf-108">Exempel 1: återskapa en nyckeln för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="fcfaf-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="fcfaf-109">Det här kommandot återskapar primär nyckeln för Azure Automation-kontot med namnet AutomationAccount01 i resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fcfaf-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="fcfaf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcfaf-110">PARAMETERS</span></span>

### <span data-ttu-id="fcfaf-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fcfaf-111">-AutomationAccountName</span></span>
<span data-ttu-id="fcfaf-112">Anger namnet på ett Automation-konto som denna cmdlet återskapar nycklar för.</span><span class="sxs-lookup"><span data-stu-id="fcfaf-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="fcfaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfaf-113">-DefaultProfile</span></span>
<span data-ttu-id="fcfaf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fcfaf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcfaf-115">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="fcfaf-115">-KeyType</span></span>
<span data-ttu-id="fcfaf-116">Anger typen för agent registrerings knappen.</span><span class="sxs-lookup"><span data-stu-id="fcfaf-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="fcfaf-117">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="fcfaf-117">Valid values are:</span></span> 
- <span data-ttu-id="fcfaf-118">Första</span><span class="sxs-lookup"><span data-stu-id="fcfaf-118">Primary</span></span> 
- <span data-ttu-id="fcfaf-119">Sekundär</span><span class="sxs-lookup"><span data-stu-id="fcfaf-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfaf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcfaf-120">-ResourceGroupName</span></span>
<span data-ttu-id="fcfaf-121">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fcfaf-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fcfaf-122">Denna cmdlet återskapar nycklar för ett Automation-konto i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="fcfaf-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fcfaf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfaf-123">CommonParameters</span></span>
<span data-ttu-id="fcfaf-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfaf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfaf-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfaf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfaf-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcfaf-126">INPUTS</span></span>

### <span data-ttu-id="fcfaf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fcfaf-127">System.String</span></span>

## <span data-ttu-id="fcfaf-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcfaf-128">OUTPUTS</span></span>

### <span data-ttu-id="fcfaf-129">Microsoft. Azure. commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="fcfaf-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="fcfaf-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcfaf-130">NOTES</span></span>

## <span data-ttu-id="fcfaf-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcfaf-131">RELATED LINKS</span></span>
