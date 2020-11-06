---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 71c910fafea0c555f5ba0d7a62573c2de2be3b41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582380"
---
# <span data-ttu-id="10580-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="10580-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="10580-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10580-102">SYNOPSIS</span></span>
<span data-ttu-id="10580-103">Tar bort ett integrerings konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10580-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10580-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10580-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10580-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10580-105">DESCRIPTION</span></span>
<span data-ttu-id="10580-106">Cmdleten **Remove-AzureRmIntegrationAccountCertificate** tar bort ett integrerings konto certifikat från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10580-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="10580-107">Ange integrerings konto namn, resurs grupps namn och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="10580-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="10580-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="10580-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="10580-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="10580-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="10580-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="10580-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="10580-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="10580-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="10580-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10580-112">EXAMPLES</span></span>

### <span data-ttu-id="10580-113">Exempel 1: ta bort ett integrerings konto certifikat</span><span class="sxs-lookup"><span data-stu-id="10580-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="10580-114">Det här kommandot tar bort integrerings konto certifikatet med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="10580-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="10580-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10580-115">PARAMETERS</span></span>

### <span data-ttu-id="10580-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="10580-116">-CertificateName</span></span>
<span data-ttu-id="10580-117">Anger namnet på ett integrations konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="10580-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="10580-118">-Force</span><span class="sxs-lookup"><span data-stu-id="10580-118">-Force</span></span>
<span data-ttu-id="10580-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="10580-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10580-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="10580-120">-Name</span></span>
<span data-ttu-id="10580-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="10580-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="10580-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10580-122">-ResourceGroupName</span></span>
<span data-ttu-id="10580-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="10580-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="10580-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10580-124">-Confirm</span></span>
<span data-ttu-id="10580-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10580-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10580-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10580-126">-WhatIf</span></span>
<span data-ttu-id="10580-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10580-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10580-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10580-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10580-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10580-129">-DefaultProfile</span></span>
<span data-ttu-id="10580-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10580-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10580-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10580-131">CommonParameters</span></span>
<span data-ttu-id="10580-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10580-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10580-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10580-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10580-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10580-134">INPUTS</span></span>

## <span data-ttu-id="10580-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10580-135">OUTPUTS</span></span>

## <span data-ttu-id="10580-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10580-136">NOTES</span></span>

## <span data-ttu-id="10580-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10580-137">RELATED LINKS</span></span>

[<span data-ttu-id="10580-138">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="10580-138">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="10580-139">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="10580-139">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="10580-140">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="10580-140">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


