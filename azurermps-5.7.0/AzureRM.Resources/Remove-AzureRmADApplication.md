---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756455"
---
# <span data-ttu-id="a36ac-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a36ac-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="a36ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a36ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a36ac-103">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="a36ac-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a36ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a36ac-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a36ac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a36ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a36ac-106">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="a36ac-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="a36ac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a36ac-107">EXAMPLES</span></span>

### <span data-ttu-id="a36ac-108">Ta bort AAD-program.</span><span class="sxs-lookup"><span data-stu-id="a36ac-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="a36ac-109">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="a36ac-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="a36ac-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a36ac-110">PARAMETERS</span></span>

### <span data-ttu-id="a36ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36ac-111">-DefaultProfile</span></span>
<span data-ttu-id="a36ac-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a36ac-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a36ac-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a36ac-113">-Force</span></span>
<span data-ttu-id="a36ac-114">Växla till att ta bort ett program utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a36ac-114">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="a36ac-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a36ac-115">-ObjectId</span></span>
<span data-ttu-id="a36ac-116">Objekt-ID för programmet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a36ac-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36ac-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a36ac-117">-Confirm</span></span>
<span data-ttu-id="a36ac-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a36ac-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36ac-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a36ac-119">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36ac-120">CommonParameters</span></span>
<span data-ttu-id="a36ac-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a36ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36ac-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a36ac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36ac-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a36ac-123">INPUTS</span></span>

### <span data-ttu-id="a36ac-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="a36ac-124">None</span></span>
<span data-ttu-id="a36ac-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a36ac-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a36ac-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a36ac-126">OUTPUTS</span></span>

## <span data-ttu-id="a36ac-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a36ac-127">NOTES</span></span>
<span data-ttu-id="a36ac-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="a36ac-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a36ac-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a36ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="a36ac-130">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a36ac-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="a36ac-131">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a36ac-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="a36ac-132">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a36ac-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="a36ac-133">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a36ac-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

