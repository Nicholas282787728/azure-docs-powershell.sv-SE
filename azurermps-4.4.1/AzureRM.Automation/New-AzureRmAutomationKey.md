---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 3b29d1b07ab0c11f42f1a7d4d9326ae19f6b79f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583859"
---
# <span data-ttu-id="82de2-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="82de2-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="82de2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82de2-102">SYNOPSIS</span></span>
<span data-ttu-id="82de2-103">Återskapar registrerings nycklar för ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="82de2-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82de2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82de2-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82de2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82de2-105">DESCRIPTION</span></span>
<span data-ttu-id="82de2-106">Cmdleten **New-AzureRmAutomationKey** återskapar registrerings nycklar för ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="82de2-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="82de2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82de2-107">EXAMPLES</span></span>

### <span data-ttu-id="82de2-108">Exempel 1: återskapa en nyckeln för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="82de2-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="82de2-109">Det här kommandot återskapar primär nyckeln för Azure Automation-kontot med namnet AutomationAccount01 i resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="82de2-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="82de2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82de2-110">PARAMETERS</span></span>

### <span data-ttu-id="82de2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82de2-111">-AutomationAccountName</span></span>
<span data-ttu-id="82de2-112">Anger namnet på ett Automation-konto som denna cmdlet återskapar nycklar för.</span><span class="sxs-lookup"><span data-stu-id="82de2-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="82de2-113">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="82de2-113">-KeyType</span></span>
<span data-ttu-id="82de2-114">Anger typen för agent registrerings knappen.</span><span class="sxs-lookup"><span data-stu-id="82de2-114">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="82de2-115">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="82de2-115">Valid values are:</span></span> 

- <span data-ttu-id="82de2-116">Första</span><span class="sxs-lookup"><span data-stu-id="82de2-116">Primary</span></span> 
- <span data-ttu-id="82de2-117">Sekundär</span><span class="sxs-lookup"><span data-stu-id="82de2-117">Secondary</span></span>

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

### <span data-ttu-id="82de2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82de2-118">-ResourceGroupName</span></span>
<span data-ttu-id="82de2-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="82de2-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="82de2-120">Denna cmdlet återskapar nycklar för ett Automation-konto i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="82de2-120">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="82de2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82de2-121">-DefaultProfile</span></span>
<span data-ttu-id="82de2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82de2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82de2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82de2-123">CommonParameters</span></span>
<span data-ttu-id="82de2-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82de2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82de2-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82de2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82de2-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82de2-126">INPUTS</span></span>

## <span data-ttu-id="82de2-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82de2-127">OUTPUTS</span></span>

### <span data-ttu-id="82de2-128">Microsoft. Azure. commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="82de2-128">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="82de2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82de2-129">NOTES</span></span>

## <span data-ttu-id="82de2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82de2-130">RELATED LINKS</span></span>

