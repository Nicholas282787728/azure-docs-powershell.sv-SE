---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581299"
---
# <span data-ttu-id="c0286-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c0286-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="c0286-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0286-102">SYNOPSIS</span></span>
<span data-ttu-id="c0286-103">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="c0286-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0286-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0286-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0286-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0286-105">DESCRIPTION</span></span>
<span data-ttu-id="c0286-106">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="c0286-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="c0286-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0286-107">EXAMPLES</span></span>

### <span data-ttu-id="c0286-108">--------------------------Ta bort AAD-program.</span><span class="sxs-lookup"><span data-stu-id="c0286-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="c0286-109">Tar bort Azure Active Directory-programmet.</span><span class="sxs-lookup"><span data-stu-id="c0286-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="c0286-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0286-110">PARAMETERS</span></span>

### <span data-ttu-id="c0286-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c0286-111">-Force</span></span>
<span data-ttu-id="c0286-112">Växla till att ta bort ett program utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c0286-112">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="c0286-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c0286-113">-ObjectId</span></span>
<span data-ttu-id="c0286-114">Objekt-ID för programmet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c0286-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0286-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0286-115">-Confirm</span></span>
<span data-ttu-id="c0286-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0286-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0286-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0286-117">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0286-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0286-118">-DefaultProfile</span></span>
<span data-ttu-id="c0286-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0286-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0286-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0286-120">CommonParameters</span></span>
<span data-ttu-id="c0286-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0286-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0286-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0286-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0286-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0286-123">INPUTS</span></span>

## <span data-ttu-id="c0286-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0286-124">OUTPUTS</span></span>

## <span data-ttu-id="c0286-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0286-125">NOTES</span></span>
<span data-ttu-id="c0286-126">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="c0286-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c0286-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0286-127">RELATED LINKS</span></span>

[<span data-ttu-id="c0286-128">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c0286-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="c0286-129">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c0286-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="c0286-130">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c0286-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="c0286-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c0286-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

