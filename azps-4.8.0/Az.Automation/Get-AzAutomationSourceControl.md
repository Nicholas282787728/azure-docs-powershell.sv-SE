---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260370"
---
# <span data-ttu-id="44465-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="44465-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="44465-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44465-102">SYNOPSIS</span></span>
<span data-ttu-id="44465-103">Hämtar en lista med käll kontroller för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="44465-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="44465-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44465-104">SYNTAX</span></span>

### <span data-ttu-id="44465-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="44465-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44465-106">ByName</span><span class="sxs-lookup"><span data-stu-id="44465-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44465-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44465-107">DESCRIPTION</span></span>
<span data-ttu-id="44465-108">Get-AzAutomationSourceControl cmdlet får kontroll för automatiserings källan.</span><span class="sxs-lookup"><span data-stu-id="44465-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="44465-109">Ange namnet på en specifik käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="44465-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="44465-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44465-110">EXAMPLES</span></span>

### <span data-ttu-id="44465-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="44465-111">Example 1</span></span>
<span data-ttu-id="44465-112">Det här kommandot får en kontroll för en automatiserings källa med namnet VSTSNative i kontot som heter devAccount.</span><span class="sxs-lookup"><span data-stu-id="44465-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="44465-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44465-113">PARAMETERS</span></span>

### <span data-ttu-id="44465-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="44465-114">-AutomationAccountName</span></span>
<span data-ttu-id="44465-115">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="44465-115">The automation account name.</span></span>

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

### <span data-ttu-id="44465-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44465-116">-DefaultProfile</span></span>
<span data-ttu-id="44465-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44465-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44465-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="44465-118">-Name</span></span>
<span data-ttu-id="44465-119">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="44465-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44465-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44465-120">-ResourceGroupName</span></span>
<span data-ttu-id="44465-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="44465-121">The resource group name.</span></span>

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

### <span data-ttu-id="44465-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="44465-122">-SourceType</span></span>
<span data-ttu-id="44465-123">Käll kontroll typen.</span><span class="sxs-lookup"><span data-stu-id="44465-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44465-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44465-124">CommonParameters</span></span>
<span data-ttu-id="44465-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44465-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44465-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44465-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44465-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44465-127">INPUTS</span></span>

### <span data-ttu-id="44465-128">System. String</span><span class="sxs-lookup"><span data-stu-id="44465-128">System.String</span></span>

## <span data-ttu-id="44465-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44465-129">OUTPUTS</span></span>

### <span data-ttu-id="44465-130">Microsoft. Azure. commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="44465-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="44465-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44465-131">NOTES</span></span>

## <span data-ttu-id="44465-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44465-132">RELATED LINKS</span></span>
