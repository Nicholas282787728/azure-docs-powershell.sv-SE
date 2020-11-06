---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: 43a405e3e3cc6bd617ba9f9dee66dd3e8902e8e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579507"
---
# <span data-ttu-id="d0022-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d0022-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="d0022-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0022-102">SYNOPSIS</span></span>
<span data-ttu-id="d0022-103">Tar bort ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="d0022-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0022-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0022-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0022-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0022-105">DESCRIPTION</span></span>
<span data-ttu-id="d0022-106">Cmdleten **Remove-AzureRmIntegrationAccount** tar bort ett integrerings konto från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d0022-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="d0022-107">Ange namnet på integrations kontot och resurs grupp namnet.</span><span class="sxs-lookup"><span data-stu-id="d0022-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="d0022-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="d0022-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d0022-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="d0022-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d0022-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="d0022-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d0022-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="d0022-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d0022-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0022-112">EXAMPLES</span></span>

### <span data-ttu-id="d0022-113">Exempel 1: ta bort ett integrations konto</span><span class="sxs-lookup"><span data-stu-id="d0022-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="d0022-114">Det här kommandot tar bort ett integrerings konto med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="d0022-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="d0022-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0022-115">PARAMETERS</span></span>

### <span data-ttu-id="d0022-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0022-116">-DefaultProfile</span></span>
<span data-ttu-id="d0022-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d0022-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0022-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d0022-118">-Force</span></span>
<span data-ttu-id="d0022-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d0022-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0022-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0022-120">-Name</span></span>
<span data-ttu-id="d0022-121">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="d0022-121">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0022-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0022-122">-ResourceGroupName</span></span>
<span data-ttu-id="d0022-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d0022-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0022-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0022-124">-Confirm</span></span>
<span data-ttu-id="d0022-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0022-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0022-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0022-126">-WhatIf</span></span>
<span data-ttu-id="d0022-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0022-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0022-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0022-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0022-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0022-129">CommonParameters</span></span>
<span data-ttu-id="d0022-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0022-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0022-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0022-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0022-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0022-132">INPUTS</span></span>

### <span data-ttu-id="d0022-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="d0022-133">None</span></span>
<span data-ttu-id="d0022-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d0022-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0022-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0022-135">OUTPUTS</span></span>

## <span data-ttu-id="d0022-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0022-136">NOTES</span></span>

## <span data-ttu-id="d0022-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0022-137">RELATED LINKS</span></span>

[<span data-ttu-id="d0022-138">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d0022-138">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="d0022-139">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d0022-139">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="d0022-140">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d0022-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


