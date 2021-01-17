---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418323"
---
# <span data-ttu-id="20b1a-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="20b1a-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="20b1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="20b1a-103">Tar bort en Azure Automation-källkod.</span><span class="sxs-lookup"><span data-stu-id="20b1a-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="20b1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20b1a-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20b1a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="20b1a-106">Remove-AzAutomationSourceControl cmdlet tar bort en käll kontroll från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="20b1a-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="20b1a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20b1a-107">EXAMPLES</span></span>

### <span data-ttu-id="20b1a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20b1a-108">Example 1</span></span>
<span data-ttu-id="20b1a-109">Det här kommandot tar bort Automation Source Control med namnet VSTSNative i kontot som heter devAccount.</span><span class="sxs-lookup"><span data-stu-id="20b1a-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="20b1a-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="20b1a-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="20b1a-111">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="20b1a-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="20b1a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20b1a-112">PARAMETERS</span></span>

### <span data-ttu-id="20b1a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20b1a-113">-AutomationAccountName</span></span>
<span data-ttu-id="20b1a-114">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="20b1a-114">The automation account name.</span></span>

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

### <span data-ttu-id="20b1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b1a-115">-DefaultProfile</span></span>
<span data-ttu-id="20b1a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20b1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b1a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="20b1a-117">-Name</span></span>
<span data-ttu-id="20b1a-118">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="20b1a-118">The source control name.</span></span>

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

### <span data-ttu-id="20b1a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20b1a-119">-PassThru</span></span>
<span data-ttu-id="20b1a-120">PassThru returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="20b1a-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20b1a-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="20b1a-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b1a-122">-ResourceGroupName</span></span>
<span data-ttu-id="20b1a-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="20b1a-123">The resource group name.</span></span>

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

### <span data-ttu-id="20b1a-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20b1a-124">-Confirm</span></span>
<span data-ttu-id="20b1a-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20b1a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b1a-126">-WhatIf</span></span>
<span data-ttu-id="20b1a-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20b1a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b1a-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20b1a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20b1a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b1a-129">CommonParameters</span></span>
<span data-ttu-id="20b1a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b1a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b1a-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b1a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b1a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20b1a-132">INPUTS</span></span>

### <span data-ttu-id="20b1a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="20b1a-133">System.String</span></span>

## <span data-ttu-id="20b1a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20b1a-134">OUTPUTS</span></span>

### <span data-ttu-id="20b1a-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="20b1a-135">System.Void</span></span>

### <span data-ttu-id="20b1a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20b1a-136">System.Boolean</span></span>

## <span data-ttu-id="20b1a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20b1a-137">NOTES</span></span>

## <span data-ttu-id="20b1a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20b1a-138">RELATED LINKS</span></span>
