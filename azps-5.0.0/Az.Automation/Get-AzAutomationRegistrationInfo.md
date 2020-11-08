---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271366"
---
# <span data-ttu-id="24d0b-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="24d0b-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="24d0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="24d0b-103">Hämtar registrerings information för att hantera en DSC-nod eller hybrid arbetare att automatisera.</span><span class="sxs-lookup"><span data-stu-id="24d0b-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="24d0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24d0b-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24d0b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24d0b-105">DESCRIPTION</span></span>
<span data-ttu-id="24d0b-106">Cmdleten **Get-AzAutomationRegistrationInfo** får den slut punkt och de nycklar som krävs för att hantera en önskad tillstånds konfiguration (DSC) eller hybrid arbetare i ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="24d0b-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="24d0b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24d0b-107">EXAMPLES</span></span>

### <span data-ttu-id="24d0b-108">Exempel 1: få registrerings information</span><span class="sxs-lookup"><span data-stu-id="24d0b-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="24d0b-109">Det här kommandot får registrerings informationen för det Automation-konto som heter AutomationAccount01 i resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="24d0b-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="24d0b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24d0b-110">PARAMETERS</span></span>

### <span data-ttu-id="24d0b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="24d0b-111">-AutomationAccountName</span></span>
<span data-ttu-id="24d0b-112">Anger namnet på Automation-kontot som denna cmdlet hämtar registrerings information för.</span><span class="sxs-lookup"><span data-stu-id="24d0b-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="24d0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d0b-113">-DefaultProfile</span></span>
<span data-ttu-id="24d0b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="24d0b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24d0b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d0b-115">-ResourceGroupName</span></span>
<span data-ttu-id="24d0b-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="24d0b-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="24d0b-117">Denna cmdlet hämtar registrerings information för den resurs grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="24d0b-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="24d0b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d0b-118">CommonParameters</span></span>
<span data-ttu-id="24d0b-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d0b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d0b-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d0b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d0b-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24d0b-121">INPUTS</span></span>

### <span data-ttu-id="24d0b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="24d0b-122">System.String</span></span>

## <span data-ttu-id="24d0b-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24d0b-123">OUTPUTS</span></span>

### <span data-ttu-id="24d0b-124">Microsoft. Azure. commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="24d0b-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="24d0b-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24d0b-125">NOTES</span></span>

## <span data-ttu-id="24d0b-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24d0b-126">RELATED LINKS</span></span>

[<span data-ttu-id="24d0b-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="24d0b-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="24d0b-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="24d0b-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="24d0b-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="24d0b-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


