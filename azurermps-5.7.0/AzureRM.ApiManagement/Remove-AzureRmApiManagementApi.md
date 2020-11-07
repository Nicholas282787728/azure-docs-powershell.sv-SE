---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: 4bcda06e1c00e338feb80584fb6e2b51a63b051d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757970"
---
# <span data-ttu-id="320e0-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="320e0-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="320e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="320e0-102">SYNOPSIS</span></span>
<span data-ttu-id="320e0-103">Tar bort ett API.</span><span class="sxs-lookup"><span data-stu-id="320e0-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="320e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="320e0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320e0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="320e0-105">DESCRIPTION</span></span>
<span data-ttu-id="320e0-106">Cmdleten **Remove-AzureRmApiManagementApi** tar bort ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="320e0-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="320e0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="320e0-107">EXAMPLES</span></span>

### <span data-ttu-id="320e0-108">Exempel 1: ta bort ett API</span><span class="sxs-lookup"><span data-stu-id="320e0-108">Example 1: Remove an API</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="320e0-109">Det här kommandot tar bort API: t med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="320e0-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="320e0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="320e0-110">PARAMETERS</span></span>

### <span data-ttu-id="320e0-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="320e0-111">-ApiId</span></span>
<span data-ttu-id="320e0-112">Anger ID: t för API Remove.</span><span class="sxs-lookup"><span data-stu-id="320e0-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="320e0-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="320e0-113">-Context</span></span>
<span data-ttu-id="320e0-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="320e0-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="320e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320e0-115">-DefaultProfile</span></span>
<span data-ttu-id="320e0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="320e0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="320e0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="320e0-117">-PassThru</span></span>
<span data-ttu-id="320e0-118">passthru</span><span class="sxs-lookup"><span data-stu-id="320e0-118">passthru</span></span>

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

### <span data-ttu-id="320e0-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="320e0-119">-Confirm</span></span>
<span data-ttu-id="320e0-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="320e0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320e0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320e0-121">-WhatIf</span></span>
<span data-ttu-id="320e0-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="320e0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320e0-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="320e0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320e0-124">CommonParameters</span></span>
<span data-ttu-id="320e0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320e0-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320e0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320e0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="320e0-127">INPUTS</span></span>

### <span data-ttu-id="320e0-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="320e0-128">None</span></span>
<span data-ttu-id="320e0-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="320e0-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="320e0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="320e0-130">OUTPUTS</span></span>

### <span data-ttu-id="320e0-131">Returtyp</span><span class="sxs-lookup"><span data-stu-id="320e0-131">Boolean</span></span>

## <span data-ttu-id="320e0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="320e0-132">NOTES</span></span>

## <span data-ttu-id="320e0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="320e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="320e0-134">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="320e0-134">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="320e0-135">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="320e0-135">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="320e0-136">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="320e0-136">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="320e0-137">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="320e0-137">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="320e0-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="320e0-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


