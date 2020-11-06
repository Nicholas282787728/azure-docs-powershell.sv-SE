---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: 7498310c232fd623b131bdf9ae59136d9a4c500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579059"
---
# <span data-ttu-id="afab6-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="afab6-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="afab6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afab6-102">SYNOPSIS</span></span>
<span data-ttu-id="afab6-103">Tar bort ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="afab6-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afab6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afab6-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afab6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afab6-105">DESCRIPTION</span></span>
<span data-ttu-id="afab6-106">Cmdleten **Remove-AzureRmAutomationCertificate** tar bort ett certifikat från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="afab6-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="afab6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afab6-107">EXAMPLES</span></span>

### <span data-ttu-id="afab6-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="afab6-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="afab6-109">Det här kommandot tar bort ett certifikat som heter Cert01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="afab6-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="afab6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afab6-110">PARAMETERS</span></span>

### <span data-ttu-id="afab6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="afab6-111">-AutomationAccountName</span></span>
<span data-ttu-id="afab6-112">Anger namnet på det Automation-konto som denna cmdlet tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="afab6-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="afab6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afab6-113">-DefaultProfile</span></span>
<span data-ttu-id="afab6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="afab6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afab6-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="afab6-115">-Name</span></span>
<span data-ttu-id="afab6-116">Anger namnet på det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="afab6-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="afab6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afab6-117">-ResourceGroupName</span></span>
<span data-ttu-id="afab6-118">Anger namnet på den resurs grupp som den här cmdleten tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="afab6-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="afab6-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afab6-119">-Confirm</span></span>
<span data-ttu-id="afab6-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afab6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afab6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afab6-121">-WhatIf</span></span>
<span data-ttu-id="afab6-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afab6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afab6-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afab6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afab6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afab6-124">CommonParameters</span></span>
<span data-ttu-id="afab6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afab6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afab6-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afab6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afab6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afab6-127">INPUTS</span></span>

### <span data-ttu-id="afab6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="afab6-128">System.String</span></span>

## <span data-ttu-id="afab6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afab6-129">OUTPUTS</span></span>

### <span data-ttu-id="afab6-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="afab6-130">System.Void</span></span>

## <span data-ttu-id="afab6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afab6-131">NOTES</span></span>

## <span data-ttu-id="afab6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afab6-132">RELATED LINKS</span></span>

[<span data-ttu-id="afab6-133">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="afab6-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="afab6-134">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="afab6-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="afab6-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="afab6-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


