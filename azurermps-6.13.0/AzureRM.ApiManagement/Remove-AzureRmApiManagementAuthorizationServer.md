---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2fc658f5bab9e6233e6b7279abc0ae80832bcc8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573068"
---
# <span data-ttu-id="c2dcb-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c2dcb-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="c2dcb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2dcb-103">Tar bort en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2dcb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2dcb-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2dcb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="c2dcb-106">Cmdleten **Remove-AzureRmApiManagementAuthorizationServer** tar bort en Azure API Management Authorization Server.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="c2dcb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2dcb-107">EXAMPLES</span></span>

## <span data-ttu-id="c2dcb-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2dcb-108">PARAMETERS</span></span>

### <span data-ttu-id="c2dcb-109">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c2dcb-109">-Context</span></span>
<span data-ttu-id="c2dcb-110">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c2dcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2dcb-111">-DefaultProfile</span></span>
<span data-ttu-id="c2dcb-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2dcb-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2dcb-113">-PassThru</span></span>
<span data-ttu-id="c2dcb-114">passthru</span><span class="sxs-lookup"><span data-stu-id="c2dcb-114">passthru</span></span>

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

### <span data-ttu-id="c2dcb-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="c2dcb-115">-ServerId</span></span>
<span data-ttu-id="c2dcb-116">Anger ID för den auktoriseringsprincip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="c2dcb-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2dcb-117">-Confirm</span></span>
<span data-ttu-id="c2dcb-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2dcb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2dcb-119">-WhatIf</span></span>
<span data-ttu-id="c2dcb-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2dcb-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2dcb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2dcb-122">CommonParameters</span></span>
<span data-ttu-id="c2dcb-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2dcb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2dcb-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2dcb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2dcb-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2dcb-125">INPUTS</span></span>

### <span data-ttu-id="c2dcb-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c2dcb-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c2dcb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c2dcb-127">System.String</span></span>

### <span data-ttu-id="c2dcb-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2dcb-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c2dcb-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2dcb-129">OUTPUTS</span></span>

### <span data-ttu-id="c2dcb-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2dcb-130">System.Boolean</span></span>

## <span data-ttu-id="c2dcb-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2dcb-131">NOTES</span></span>

## <span data-ttu-id="c2dcb-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2dcb-132">RELATED LINKS</span></span>

[<span data-ttu-id="c2dcb-133">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c2dcb-133">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="c2dcb-134">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c2dcb-134">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="c2dcb-135">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c2dcb-135">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


