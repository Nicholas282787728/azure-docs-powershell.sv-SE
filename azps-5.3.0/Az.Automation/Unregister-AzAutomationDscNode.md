---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524836"
---
# <span data-ttu-id="fb2d9-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fb2d9-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="fb2d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2d9-103">Tar bort en DSC-nod från hanteringen av ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="fb2d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb2d9-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb2d9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb2d9-105">DESCRIPTION</span></span>
<span data-ttu-id="fb2d9-106">Med cmdleten **Unregistered-AzAutomationDscNode** tar du bort en APS-nod för önskad tillstånds konfiguration (DSC) från hantering av ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="fb2d9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb2d9-107">EXAMPLES</span></span>

### <span data-ttu-id="fb2d9-108">Exempel 1: ta bort en Azure DSC-nod från hantering med ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="fb2d9-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="fb2d9-109">Det här kommandot tar bort DSC-noden med angivet GUID från hanteringen av Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="fb2d9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb2d9-110">PARAMETERS</span></span>

### <span data-ttu-id="fb2d9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fb2d9-111">-AutomationAccountName</span></span>
<span data-ttu-id="fb2d9-112">Anger namnet på det Automation-konto som den här cmdleten tar bort en DSC-nod från.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="fb2d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2d9-113">-DefaultProfile</span></span>
<span data-ttu-id="fb2d9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fb2d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb2d9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fb2d9-115">-Force</span></span>
<span data-ttu-id="fb2d9-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="fb2d9-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2d9-117">-ID</span><span class="sxs-lookup"><span data-stu-id="fb2d9-117">-Id</span></span>
<span data-ttu-id="fb2d9-118">Anger unikt ID för DSC-noden som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb2d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb2d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb2d9-120">Anger namnet på en resurs grupp där denna cmdlet avregistrerar en DSC-nod.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="fb2d9-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb2d9-121">-Confirm</span></span>
<span data-ttu-id="fb2d9-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb2d9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb2d9-123">-WhatIf</span></span>
<span data-ttu-id="fb2d9-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb2d9-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb2d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2d9-126">CommonParameters</span></span>
<span data-ttu-id="fb2d9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb2d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2d9-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb2d9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2d9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb2d9-129">INPUTS</span></span>

### <span data-ttu-id="fb2d9-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fb2d9-130">System.Guid</span></span>

### <span data-ttu-id="fb2d9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fb2d9-131">System.String</span></span>

## <span data-ttu-id="fb2d9-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb2d9-132">OUTPUTS</span></span>

### <span data-ttu-id="fb2d9-133">Microsoft. Azure. commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="fb2d9-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="fb2d9-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb2d9-134">NOTES</span></span>

## <span data-ttu-id="fb2d9-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb2d9-135">RELATED LINKS</span></span>

[<span data-ttu-id="fb2d9-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fb2d9-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="fb2d9-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fb2d9-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="fb2d9-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="fb2d9-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


