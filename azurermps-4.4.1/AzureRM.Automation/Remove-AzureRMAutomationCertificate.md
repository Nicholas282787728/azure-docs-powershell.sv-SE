---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579823"
---
# <span data-ttu-id="3972e-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3972e-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="3972e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3972e-102">SYNOPSIS</span></span>
<span data-ttu-id="3972e-103">Tar bort ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="3972e-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3972e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3972e-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3972e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3972e-105">DESCRIPTION</span></span>
<span data-ttu-id="3972e-106">Cmdleten **Remove-AzureRmAutomationCertificate** tar bort ett certifikat från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3972e-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="3972e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3972e-107">EXAMPLES</span></span>

### <span data-ttu-id="3972e-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="3972e-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3972e-109">Det här kommandot tar bort ett certifikat som heter Cert01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3972e-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3972e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3972e-110">PARAMETERS</span></span>

### <span data-ttu-id="3972e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3972e-111">-AutomationAccountName</span></span>
<span data-ttu-id="3972e-112">Anger namnet på det Automation-konto som denna cmdlet tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="3972e-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="3972e-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3972e-113">-Name</span></span>
<span data-ttu-id="3972e-114">Anger namnet på det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="3972e-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3972e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3972e-115">-ResourceGroupName</span></span>
<span data-ttu-id="3972e-116">Anger namnet på den resurs grupp som den här cmdleten tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="3972e-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="3972e-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3972e-117">-Confirm</span></span>
<span data-ttu-id="3972e-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3972e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3972e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3972e-119">-WhatIf</span></span>
<span data-ttu-id="3972e-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3972e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3972e-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3972e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3972e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3972e-122">-DefaultProfile</span></span>
<span data-ttu-id="3972e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3972e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3972e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3972e-124">CommonParameters</span></span>
<span data-ttu-id="3972e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3972e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3972e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3972e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3972e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3972e-127">INPUTS</span></span>

## <span data-ttu-id="3972e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3972e-128">OUTPUTS</span></span>

## <span data-ttu-id="3972e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3972e-129">NOTES</span></span>

## <span data-ttu-id="3972e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3972e-130">RELATED LINKS</span></span>

[<span data-ttu-id="3972e-131">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3972e-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3972e-132">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3972e-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3972e-133">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3972e-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


