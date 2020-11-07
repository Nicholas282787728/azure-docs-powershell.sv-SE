---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 1d0587ae9d1d45de4f08b71baa48ebb5e1633a36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754798"
---
# <span data-ttu-id="d9a3d-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="d9a3d-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="d9a3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a3d-103">Återskapar registrerings nycklar för ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="d9a3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9a3d-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9a3d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="d9a3d-106">Cmdleten **New-AzAutomationKey** återskapar registrerings nycklar för ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="d9a3d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9a3d-107">EXAMPLES</span></span>

### <span data-ttu-id="d9a3d-108">Exempel 1: återskapa en nyckeln för ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="d9a3d-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="d9a3d-109">Det här kommandot återskapar primär nyckeln för Azure Automation-kontot med namnet AutomationAccount01 i resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d9a3d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9a3d-110">PARAMETERS</span></span>

### <span data-ttu-id="d9a3d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9a3d-111">-AutomationAccountName</span></span>
<span data-ttu-id="d9a3d-112">Anger namnet på ett Automation-konto som denna cmdlet återskapar nycklar för.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="d9a3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a3d-113">-DefaultProfile</span></span>
<span data-ttu-id="d9a3d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d9a3d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9a3d-115">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="d9a3d-115">-KeyType</span></span>
<span data-ttu-id="d9a3d-116">Anger typen för agent registrerings knappen.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="d9a3d-117">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="d9a3d-117">Valid values are:</span></span> 
- <span data-ttu-id="d9a3d-118">Första</span><span class="sxs-lookup"><span data-stu-id="d9a3d-118">Primary</span></span> 
- <span data-ttu-id="d9a3d-119">Sekundär</span><span class="sxs-lookup"><span data-stu-id="d9a3d-119">Secondary</span></span>

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

### <span data-ttu-id="d9a3d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a3d-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9a3d-121">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d9a3d-122">Denna cmdlet återskapar nycklar för ett Automation-konto i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9a3d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a3d-123">CommonParameters</span></span>
<span data-ttu-id="d9a3d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a3d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a3d-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a3d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a3d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9a3d-126">INPUTS</span></span>

### <span data-ttu-id="d9a3d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d9a3d-127">System.String</span></span>

## <span data-ttu-id="d9a3d-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9a3d-128">OUTPUTS</span></span>

### <span data-ttu-id="d9a3d-129">Microsoft. Azure. commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="d9a3d-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="d9a3d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9a3d-130">NOTES</span></span>

## <span data-ttu-id="d9a3d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9a3d-131">RELATED LINKS</span></span>