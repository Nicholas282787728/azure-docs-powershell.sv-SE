---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cadae96af05ae11f76d3a8ea0010da4d73161186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573773"
---
# <span data-ttu-id="905e8-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="905e8-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="905e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="905e8-102">SYNOPSIS</span></span>
<span data-ttu-id="905e8-103">Tar bort ett API.</span><span class="sxs-lookup"><span data-stu-id="905e8-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="905e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="905e8-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="905e8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="905e8-105">DESCRIPTION</span></span>
<span data-ttu-id="905e8-106">Cmdleten **Remove-AzureRmApiManagementApi** tar bort ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="905e8-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="905e8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="905e8-107">EXAMPLES</span></span>

### <span data-ttu-id="905e8-108">Exempel 1: ta bort ett API</span><span class="sxs-lookup"><span data-stu-id="905e8-108">Example 1: Remove an API</span></span>
```
PS C:\>Remove-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789"
```

<span data-ttu-id="905e8-109">Det här kommandot tar bort API: t med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="905e8-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="905e8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="905e8-110">PARAMETERS</span></span>

### <span data-ttu-id="905e8-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="905e8-111">-ApiId</span></span>
<span data-ttu-id="905e8-112">Anger ID: t för API Remove.</span><span class="sxs-lookup"><span data-stu-id="905e8-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="905e8-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="905e8-113">-Context</span></span>
<span data-ttu-id="905e8-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="905e8-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="905e8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="905e8-115">-PassThru</span></span>
<span data-ttu-id="905e8-116">passthru</span><span class="sxs-lookup"><span data-stu-id="905e8-116">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="905e8-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="905e8-117">-Confirm</span></span>
<span data-ttu-id="905e8-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="905e8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="905e8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="905e8-119">-WhatIf</span></span>
<span data-ttu-id="905e8-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="905e8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="905e8-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="905e8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="905e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905e8-122">-DefaultProfile</span></span>
<span data-ttu-id="905e8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="905e8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="905e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905e8-124">CommonParameters</span></span>
<span data-ttu-id="905e8-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905e8-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905e8-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="905e8-127">INPUTS</span></span>

## <span data-ttu-id="905e8-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="905e8-128">OUTPUTS</span></span>

### <span data-ttu-id="905e8-129">Returtyp</span><span class="sxs-lookup"><span data-stu-id="905e8-129">Boolean</span></span>

## <span data-ttu-id="905e8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="905e8-130">NOTES</span></span>

## <span data-ttu-id="905e8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="905e8-131">RELATED LINKS</span></span>

[<span data-ttu-id="905e8-132">Exportera-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="905e8-132">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="905e8-133">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="905e8-133">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="905e8-134">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="905e8-134">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="905e8-135">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="905e8-135">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="905e8-136">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="905e8-136">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


