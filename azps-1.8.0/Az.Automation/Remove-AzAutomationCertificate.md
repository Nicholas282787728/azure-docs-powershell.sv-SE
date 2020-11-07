---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: 9932627e94a27c1b29d20a5a6bc49d47a55d3ef5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754773"
---
# <span data-ttu-id="0e544-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e544-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="0e544-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e544-102">SYNOPSIS</span></span>
<span data-ttu-id="0e544-103">Tar bort ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="0e544-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="0e544-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e544-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e544-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e544-105">DESCRIPTION</span></span>
<span data-ttu-id="0e544-106">Cmdleten **Remove-AzAutomationCertificate** tar bort ett certifikat från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0e544-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="0e544-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e544-107">EXAMPLES</span></span>

### <span data-ttu-id="0e544-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="0e544-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0e544-109">Det här kommandot tar bort ett certifikat som heter Cert01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0e544-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0e544-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e544-110">PARAMETERS</span></span>

### <span data-ttu-id="0e544-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0e544-111">-AutomationAccountName</span></span>
<span data-ttu-id="0e544-112">Anger namnet på det Automation-konto som denna cmdlet tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="0e544-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="0e544-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e544-113">-DefaultProfile</span></span>
<span data-ttu-id="0e544-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0e544-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e544-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e544-115">-Name</span></span>
<span data-ttu-id="0e544-116">Anger namnet på det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0e544-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0e544-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e544-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e544-118">Anger namnet på den resurs grupp som den här cmdleten tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="0e544-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="0e544-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e544-119">-Confirm</span></span>
<span data-ttu-id="0e544-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e544-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e544-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e544-121">-WhatIf</span></span>
<span data-ttu-id="0e544-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e544-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e544-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e544-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e544-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e544-124">CommonParameters</span></span>
<span data-ttu-id="0e544-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e544-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e544-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e544-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e544-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e544-127">INPUTS</span></span>

### <span data-ttu-id="0e544-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0e544-128">System.String</span></span>

## <span data-ttu-id="0e544-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e544-129">OUTPUTS</span></span>

### <span data-ttu-id="0e544-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="0e544-130">System.Void</span></span>

## <span data-ttu-id="0e544-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e544-131">NOTES</span></span>

## <span data-ttu-id="0e544-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e544-132">RELATED LINKS</span></span>

[<span data-ttu-id="0e544-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e544-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="0e544-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e544-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="0e544-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e544-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


