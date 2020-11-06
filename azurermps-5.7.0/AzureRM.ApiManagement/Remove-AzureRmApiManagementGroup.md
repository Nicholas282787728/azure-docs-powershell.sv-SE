---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: a5919959f038b94a27f373124377466926494337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583711"
---
# <span data-ttu-id="12878-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="12878-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="12878-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12878-102">SYNOPSIS</span></span>
<span data-ttu-id="12878-103">Tar bort en befintlig API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="12878-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12878-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12878-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12878-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12878-105">DESCRIPTION</span></span>
<span data-ttu-id="12878-106">Cmdleten **Remove-AzureRmApiManagementGroup** tar bort en befintlig API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="12878-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="12878-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12878-107">EXAMPLES</span></span>

### <span data-ttu-id="12878-108">Exempel 1: ta bort en befintlig hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="12878-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="12878-109">Det här kommandot tar bort en befintlig hanterings grupp med namnet Group0001 och ber inte användaren att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="12878-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="12878-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12878-110">PARAMETERS</span></span>

### <span data-ttu-id="12878-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="12878-111">-Context</span></span>
<span data-ttu-id="12878-112">Anger förekomsten av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="12878-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12878-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12878-113">-DefaultProfile</span></span>
<span data-ttu-id="12878-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12878-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="12878-115">-Kund-</span><span class="sxs-lookup"><span data-stu-id="12878-115">-GroupId</span></span>
<span data-ttu-id="12878-116">Anger ID: till en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="12878-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="12878-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12878-117">-PassThru</span></span>
<span data-ttu-id="12878-118">Anger att denna cmdlet returnerar ett värde för $True om det lyckas, eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="12878-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12878-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12878-119">-Confirm</span></span>
<span data-ttu-id="12878-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12878-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12878-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12878-121">-WhatIf</span></span>
<span data-ttu-id="12878-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12878-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12878-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12878-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12878-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12878-124">CommonParameters</span></span>
<span data-ttu-id="12878-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12878-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12878-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12878-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12878-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12878-127">INPUTS</span></span>

### <span data-ttu-id="12878-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="12878-128">None</span></span>
<span data-ttu-id="12878-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="12878-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12878-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12878-130">OUTPUTS</span></span>

### <span data-ttu-id="12878-131">Returtyp</span><span class="sxs-lookup"><span data-stu-id="12878-131">Boolean</span></span>

## <span data-ttu-id="12878-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12878-132">NOTES</span></span>

## <span data-ttu-id="12878-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12878-133">RELATED LINKS</span></span>

[<span data-ttu-id="12878-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="12878-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="12878-135">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="12878-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="12878-136">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="12878-136">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


