---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092600"
---
# <span data-ttu-id="ba206-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ba206-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="ba206-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba206-102">SYNOPSIS</span></span>
<span data-ttu-id="ba206-103">Tar bort ett integrerings konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ba206-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="ba206-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba206-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba206-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba206-105">DESCRIPTION</span></span>
<span data-ttu-id="ba206-106">Cmdleten **Remove-AzIntegrationAccountCertificate** tar bort ett integrerings konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ba206-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="ba206-107">Ange integrerings konto namn, resurs grupps namn och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="ba206-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="ba206-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="ba206-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ba206-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="ba206-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ba206-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="ba206-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ba206-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="ba206-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ba206-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba206-112">EXAMPLES</span></span>

### <span data-ttu-id="ba206-113">Exempel 1: ta bort ett integrerings konto certifikat</span><span class="sxs-lookup"><span data-stu-id="ba206-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="ba206-114">Det här kommandot tar bort integrerings konto certifikatet med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="ba206-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="ba206-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba206-115">PARAMETERS</span></span>

### <span data-ttu-id="ba206-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ba206-116">-CertificateName</span></span>
<span data-ttu-id="ba206-117">Anger namnet på ett integrations konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="ba206-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="ba206-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba206-118">-DefaultProfile</span></span>
<span data-ttu-id="ba206-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ba206-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba206-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ba206-120">-Force</span></span>
<span data-ttu-id="ba206-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ba206-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba206-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba206-122">-Name</span></span>
<span data-ttu-id="ba206-123">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="ba206-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ba206-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba206-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba206-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ba206-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ba206-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ba206-126">-Confirm</span></span>
<span data-ttu-id="ba206-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba206-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba206-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba206-128">-WhatIf</span></span>
<span data-ttu-id="ba206-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ba206-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba206-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ba206-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba206-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba206-131">CommonParameters</span></span>
<span data-ttu-id="ba206-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba206-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba206-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba206-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba206-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba206-134">INPUTS</span></span>

### <span data-ttu-id="ba206-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ba206-135">System.String</span></span>

## <span data-ttu-id="ba206-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba206-136">OUTPUTS</span></span>

### <span data-ttu-id="ba206-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="ba206-137">System.Void</span></span>

## <span data-ttu-id="ba206-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba206-138">NOTES</span></span>

## <span data-ttu-id="ba206-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba206-139">RELATED LINKS</span></span>

[<span data-ttu-id="ba206-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ba206-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="ba206-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ba206-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="ba206-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ba206-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)

