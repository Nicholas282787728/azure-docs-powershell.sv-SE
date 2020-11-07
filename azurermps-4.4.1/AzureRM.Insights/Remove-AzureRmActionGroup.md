---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 0b5f84a38fcd087b77b32624b9cbd9b3b8a27e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757787"
---
# <span data-ttu-id="4be26-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4be26-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="4be26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4be26-102">SYNOPSIS</span></span>
<span data-ttu-id="4be26-103">Tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="4be26-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4be26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4be26-104">SYNTAX</span></span>

### <span data-ttu-id="4be26-105">ByPropertyName (standard)</span><span class="sxs-lookup"><span data-stu-id="4be26-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be26-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4be26-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4be26-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4be26-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be26-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4be26-108">DESCRIPTION</span></span>
<span data-ttu-id="4be26-109">Cmdleten **Remove-AzureRmActionGroup** tar bort en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="4be26-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="4be26-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4be26-110">EXAMPLES</span></span>

### <span data-ttu-id="4be26-111">Exempel 1: ta bort en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="4be26-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="4be26-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4be26-112">PARAMETERS</span></span>

### <span data-ttu-id="4be26-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4be26-113">-Name</span></span>
<span data-ttu-id="4be26-114">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="4be26-114">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be26-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4be26-115">-Confirm</span></span>
<span data-ttu-id="4be26-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4be26-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be26-117">-DefaultProfile</span></span>
<span data-ttu-id="4be26-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4be26-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4be26-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4be26-119">-InputObject</span></span>
<span data-ttu-id="4be26-120">Resurs för åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="4be26-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4be26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be26-121">-ResourceGroupName</span></span>
<span data-ttu-id="4be26-122">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="4be26-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be26-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4be26-123">-ResourceId</span></span>
<span data-ttu-id="4be26-124">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="4be26-124">The resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be26-125">-WhatIf</span></span>
<span data-ttu-id="4be26-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4be26-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4be26-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4be26-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be26-128">CommonParameters</span></span>
<span data-ttu-id="4be26-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be26-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be26-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be26-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4be26-131">INPUTS</span></span>

## <span data-ttu-id="4be26-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4be26-132">OUTPUTS</span></span>

### <span data-ttu-id="4be26-133">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4be26-133">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4be26-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4be26-134">NOTES</span></span>

## <span data-ttu-id="4be26-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4be26-135">RELATED LINKS</span></span>

<span data-ttu-id="4be26-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="4be26-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
