---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: dfdd4d4de935d83beaa20246c490ded7b23dcc9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573564"
---
# <span data-ttu-id="bdd82-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="bdd82-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="bdd82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bdd82-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd82-103">Hämtar registrerings information för att hantera en DSC-nod eller hybrid arbetare att automatisera.</span><span class="sxs-lookup"><span data-stu-id="bdd82-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bdd82-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdd82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bdd82-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd82-106">Cmdleten **Get-AzureRmAutomationRegistrationInfo** får den slut punkt och de nycklar som krävs för att hantera en önskad tillstånds konfiguration (DSC) eller hybrid arbetare i ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="bdd82-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="bdd82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bdd82-107">EXAMPLES</span></span>

### <span data-ttu-id="bdd82-108">Exempel 1: få registrerings information</span><span class="sxs-lookup"><span data-stu-id="bdd82-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="bdd82-109">Det här kommandot får registrerings informationen för det Automation-konto som heter AutomationAccount01 i resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="bdd82-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="bdd82-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bdd82-110">PARAMETERS</span></span>

### <span data-ttu-id="bdd82-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bdd82-111">-AutomationAccountName</span></span>
<span data-ttu-id="bdd82-112">Anger namnet på Automation-kontot som denna cmdlet hämtar registrerings information för.</span><span class="sxs-lookup"><span data-stu-id="bdd82-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="bdd82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd82-113">-DefaultProfile</span></span>
<span data-ttu-id="bdd82-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bdd82-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdd82-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd82-115">-ResourceGroupName</span></span>
<span data-ttu-id="bdd82-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bdd82-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bdd82-117">Denna cmdlet hämtar registrerings information för den resurs grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bdd82-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdd82-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd82-118">CommonParameters</span></span>
<span data-ttu-id="bdd82-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd82-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd82-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd82-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd82-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bdd82-121">INPUTS</span></span>

### <span data-ttu-id="bdd82-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="bdd82-122">None</span></span>
<span data-ttu-id="bdd82-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bdd82-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bdd82-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bdd82-124">OUTPUTS</span></span>

### <span data-ttu-id="bdd82-125">Microsoft. Azure. commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="bdd82-125">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="bdd82-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bdd82-126">NOTES</span></span>

## <span data-ttu-id="bdd82-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bdd82-127">RELATED LINKS</span></span>

[<span data-ttu-id="bdd82-128">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bdd82-128">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="bdd82-129">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="bdd82-129">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="bdd82-130">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="bdd82-130">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)

