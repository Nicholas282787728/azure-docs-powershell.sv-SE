---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 9e857d506b149c79d86ca52f2d3d7d3e3d598216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743758"
---
# <span data-ttu-id="f448e-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f448e-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="f448e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f448e-102">SYNOPSIS</span></span>
<span data-ttu-id="f448e-103">Tar bort ett integrerings konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f448e-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="f448e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f448e-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f448e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f448e-105">DESCRIPTION</span></span>
<span data-ttu-id="f448e-106">Cmdleten **Remove-AzIntegrationAccountCertificate** tar bort ett integrerings konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f448e-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="f448e-107">Ange integrerings konto namn, resurs grupps namn och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="f448e-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="f448e-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="f448e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f448e-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="f448e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f448e-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f448e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f448e-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="f448e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f448e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f448e-112">EXAMPLES</span></span>

### <span data-ttu-id="f448e-113">Exempel 1: ta bort ett integrerings konto certifikat</span><span class="sxs-lookup"><span data-stu-id="f448e-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="f448e-114">Det här kommandot tar bort integrerings konto certifikatet med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="f448e-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="f448e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f448e-115">PARAMETERS</span></span>

### <span data-ttu-id="f448e-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="f448e-116">-CertificateName</span></span>
<span data-ttu-id="f448e-117">Anger namnet på ett integrations konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="f448e-117">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f448e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f448e-118">-DefaultProfile</span></span>
<span data-ttu-id="f448e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f448e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f448e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f448e-120">-Force</span></span>
<span data-ttu-id="f448e-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f448e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f448e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="f448e-122">-Name</span></span>
<span data-ttu-id="f448e-123">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="f448e-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f448e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f448e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f448e-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f448e-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f448e-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f448e-126">-Confirm</span></span>
<span data-ttu-id="f448e-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f448e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f448e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f448e-128">-WhatIf</span></span>
<span data-ttu-id="f448e-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f448e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f448e-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f448e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f448e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f448e-131">CommonParameters</span></span>
<span data-ttu-id="f448e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f448e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f448e-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f448e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f448e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f448e-134">INPUTS</span></span>

### <span data-ttu-id="f448e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f448e-135">System.String</span></span>

## <span data-ttu-id="f448e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f448e-136">OUTPUTS</span></span>

### <span data-ttu-id="f448e-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="f448e-137">System.Void</span></span>

## <span data-ttu-id="f448e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f448e-138">NOTES</span></span>

## <span data-ttu-id="f448e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f448e-139">RELATED LINKS</span></span>

[<span data-ttu-id="f448e-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f448e-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="f448e-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f448e-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="f448e-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f448e-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)

