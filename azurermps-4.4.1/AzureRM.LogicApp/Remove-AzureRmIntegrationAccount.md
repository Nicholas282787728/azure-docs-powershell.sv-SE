---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: eb78395274171f448076a4cd3ad9b6bac0093301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758394"
---
# <span data-ttu-id="9c056-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9c056-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="9c056-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c056-102">SYNOPSIS</span></span>
<span data-ttu-id="9c056-103">Tar bort ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="9c056-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c056-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c056-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c056-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c056-105">DESCRIPTION</span></span>
<span data-ttu-id="9c056-106">Cmdleten **Remove-AzureRmIntegrationAccount** tar bort ett integrerings konto från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9c056-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="9c056-107">Ange namnet på integrations kontot och resurs grupp namnet.</span><span class="sxs-lookup"><span data-stu-id="9c056-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="9c056-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="9c056-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9c056-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="9c056-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9c056-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="9c056-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9c056-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="9c056-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9c056-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c056-112">EXAMPLES</span></span>

### <span data-ttu-id="9c056-113">Exempel 1: ta bort ett integrations konto</span><span class="sxs-lookup"><span data-stu-id="9c056-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="9c056-114">Det här kommandot tar bort ett integrerings konto med namnet IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="9c056-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="9c056-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c056-115">PARAMETERS</span></span>

### <span data-ttu-id="9c056-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9c056-116">-Force</span></span>
<span data-ttu-id="9c056-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9c056-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c056-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c056-118">-Name</span></span>
<span data-ttu-id="9c056-119">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="9c056-119">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="9c056-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c056-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c056-121">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9c056-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9c056-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c056-122">-Confirm</span></span>
<span data-ttu-id="9c056-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c056-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c056-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c056-124">-WhatIf</span></span>
<span data-ttu-id="9c056-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c056-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c056-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c056-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c056-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c056-127">-DefaultProfile</span></span>
<span data-ttu-id="9c056-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c056-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c056-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c056-129">CommonParameters</span></span>
<span data-ttu-id="9c056-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c056-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c056-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c056-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c056-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c056-132">INPUTS</span></span>

## <span data-ttu-id="9c056-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c056-133">OUTPUTS</span></span>

## <span data-ttu-id="9c056-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c056-134">NOTES</span></span>

## <span data-ttu-id="9c056-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c056-135">RELATED LINKS</span></span>

[<span data-ttu-id="9c056-136">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9c056-136">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="9c056-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9c056-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="9c056-138">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="9c056-138">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


