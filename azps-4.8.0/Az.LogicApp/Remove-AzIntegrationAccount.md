---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259554"
---
# <span data-ttu-id="cf22d-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cf22d-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="cf22d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf22d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf22d-103">Tar bort ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="cf22d-103">Removes an integration account.</span></span>

## <span data-ttu-id="cf22d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf22d-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf22d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf22d-105">DESCRIPTION</span></span>
<span data-ttu-id="cf22d-106">Cmdleten **Remove-AzIntegrationAccount** tar bort ett integrerings konto från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cf22d-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="cf22d-107">Ange namnet på integrations kontot och resurs grupp namnet.</span><span class="sxs-lookup"><span data-stu-id="cf22d-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="cf22d-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="cf22d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cf22d-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="cf22d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cf22d-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="cf22d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cf22d-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="cf22d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cf22d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf22d-112">EXAMPLES</span></span>

### <span data-ttu-id="cf22d-113">Exempel 1: ta bort ett integrations konto</span><span class="sxs-lookup"><span data-stu-id="cf22d-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="cf22d-114">Det här kommandot tar bort ett integrerings konto med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="cf22d-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="cf22d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf22d-115">PARAMETERS</span></span>

### <span data-ttu-id="cf22d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf22d-116">-DefaultProfile</span></span>
<span data-ttu-id="cf22d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cf22d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf22d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cf22d-118">-Force</span></span>
<span data-ttu-id="cf22d-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cf22d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf22d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf22d-120">-Name</span></span>
<span data-ttu-id="cf22d-121">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="cf22d-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="cf22d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf22d-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf22d-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cf22d-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cf22d-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cf22d-124">-Confirm</span></span>
<span data-ttu-id="cf22d-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cf22d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf22d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf22d-126">-WhatIf</span></span>
<span data-ttu-id="cf22d-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cf22d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf22d-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cf22d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf22d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf22d-129">CommonParameters</span></span>
<span data-ttu-id="cf22d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf22d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf22d-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf22d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf22d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf22d-132">INPUTS</span></span>

### <span data-ttu-id="cf22d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cf22d-133">System.String</span></span>

## <span data-ttu-id="cf22d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf22d-134">OUTPUTS</span></span>

### <span data-ttu-id="cf22d-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="cf22d-135">System.Void</span></span>

## <span data-ttu-id="cf22d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf22d-136">NOTES</span></span>

## <span data-ttu-id="cf22d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf22d-137">RELATED LINKS</span></span>

[<span data-ttu-id="cf22d-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cf22d-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="cf22d-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cf22d-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="cf22d-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cf22d-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


