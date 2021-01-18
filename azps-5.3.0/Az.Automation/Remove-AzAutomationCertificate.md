---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524908"
---
# <span data-ttu-id="a320a-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a320a-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="a320a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a320a-102">SYNOPSIS</span></span>
<span data-ttu-id="a320a-103">Tar bort ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="a320a-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="a320a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a320a-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a320a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a320a-105">DESCRIPTION</span></span>
<span data-ttu-id="a320a-106">Cmdleten **Remove-AzAutomationCertificate** tar bort ett certifikat från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a320a-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="a320a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a320a-107">EXAMPLES</span></span>

### <span data-ttu-id="a320a-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="a320a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a320a-109">Det här kommandot tar bort ett certifikat som heter Cert01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a320a-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a320a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a320a-110">PARAMETERS</span></span>

### <span data-ttu-id="a320a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a320a-111">-AutomationAccountName</span></span>
<span data-ttu-id="a320a-112">Anger namnet på det Automation-konto som denna cmdlet tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="a320a-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="a320a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a320a-113">-DefaultProfile</span></span>
<span data-ttu-id="a320a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a320a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a320a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a320a-115">-Name</span></span>
<span data-ttu-id="a320a-116">Anger namnet på det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a320a-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a320a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a320a-117">-ResourceGroupName</span></span>
<span data-ttu-id="a320a-118">Anger namnet på den resurs grupp som den här cmdleten tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="a320a-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="a320a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a320a-119">-Confirm</span></span>
<span data-ttu-id="a320a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a320a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a320a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a320a-121">-WhatIf</span></span>
<span data-ttu-id="a320a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a320a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a320a-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a320a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a320a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a320a-124">CommonParameters</span></span>
<span data-ttu-id="a320a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a320a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a320a-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a320a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a320a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a320a-127">INPUTS</span></span>

### <span data-ttu-id="a320a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a320a-128">System.String</span></span>

## <span data-ttu-id="a320a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a320a-129">OUTPUTS</span></span>

### <span data-ttu-id="a320a-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="a320a-130">System.Void</span></span>

## <span data-ttu-id="a320a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a320a-131">NOTES</span></span>

## <span data-ttu-id="a320a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a320a-132">RELATED LINKS</span></span>

[<span data-ttu-id="a320a-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a320a-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="a320a-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a320a-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="a320a-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a320a-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


