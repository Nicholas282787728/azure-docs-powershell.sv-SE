---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: e960b1d68b57ef51ef51a6bd00365242e78f47a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754821"
---
# <span data-ttu-id="a4276-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="a4276-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="a4276-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4276-102">SYNOPSIS</span></span>
<span data-ttu-id="a4276-103">Hämtar en lista med käll kontroller för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a4276-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="a4276-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4276-104">SYNTAX</span></span>

### <span data-ttu-id="a4276-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="a4276-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4276-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a4276-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4276-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4276-107">DESCRIPTION</span></span>
<span data-ttu-id="a4276-108">Get-AzAutomationSourceControl cmdlet får kontroll för automatiserings källan.</span><span class="sxs-lookup"><span data-stu-id="a4276-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="a4276-109">Ange namnet på en specifik käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="a4276-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="a4276-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4276-110">EXAMPLES</span></span>

### <span data-ttu-id="a4276-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4276-111">Example 1</span></span>
<span data-ttu-id="a4276-112">Det här kommandot får en kontroll för en automatiserings källa med namnet VSTSNative i kontot som heter devAccount.</span><span class="sxs-lookup"><span data-stu-id="a4276-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="a4276-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4276-113">PARAMETERS</span></span>

### <span data-ttu-id="a4276-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a4276-114">-AutomationAccountName</span></span>
<span data-ttu-id="a4276-115">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="a4276-115">The automation account name.</span></span>

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

### <span data-ttu-id="a4276-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4276-116">-DefaultProfile</span></span>
<span data-ttu-id="a4276-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4276-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4276-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4276-118">-Name</span></span>
<span data-ttu-id="a4276-119">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="a4276-119">The source control name.</span></span>

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

### <span data-ttu-id="a4276-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4276-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4276-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a4276-121">The resource group name.</span></span>

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

### <span data-ttu-id="a4276-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="a4276-122">-SourceType</span></span>
<span data-ttu-id="a4276-123">Käll kontroll typen.</span><span class="sxs-lookup"><span data-stu-id="a4276-123">The source control type.</span></span>

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

### <span data-ttu-id="a4276-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4276-124">CommonParameters</span></span>
<span data-ttu-id="a4276-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4276-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4276-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4276-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4276-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4276-127">INPUTS</span></span>

### <span data-ttu-id="a4276-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a4276-128">System.String</span></span>

## <span data-ttu-id="a4276-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4276-129">OUTPUTS</span></span>

### <span data-ttu-id="a4276-130">Microsoft. Azure. commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="a4276-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="a4276-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4276-131">NOTES</span></span>

## <span data-ttu-id="a4276-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4276-132">RELATED LINKS</span></span>