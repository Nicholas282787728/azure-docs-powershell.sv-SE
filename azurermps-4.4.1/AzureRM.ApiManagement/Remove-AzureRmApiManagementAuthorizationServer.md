---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 16a48b6f945aac8ef287ff612d64da1273add521
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573769"
---
# <span data-ttu-id="167a1-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="167a1-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="167a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="167a1-102">SYNOPSIS</span></span>
<span data-ttu-id="167a1-103">Tar bort en auktoriseringsprincip.</span><span class="sxs-lookup"><span data-stu-id="167a1-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="167a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="167a1-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="167a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="167a1-105">DESCRIPTION</span></span>
<span data-ttu-id="167a1-106">Cmdleten **Remove-AzureRmApiManagementAuthorizationServer** tar bort en Azure API Management Authorization Server.</span><span class="sxs-lookup"><span data-stu-id="167a1-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="167a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="167a1-107">EXAMPLES</span></span>

## <span data-ttu-id="167a1-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="167a1-108">PARAMETERS</span></span>

### <span data-ttu-id="167a1-109">-Kontext</span><span class="sxs-lookup"><span data-stu-id="167a1-109">-Context</span></span>
<span data-ttu-id="167a1-110">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="167a1-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="167a1-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="167a1-111">-PassThru</span></span>
<span data-ttu-id="167a1-112">passthru</span><span class="sxs-lookup"><span data-stu-id="167a1-112">passthru</span></span>

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

### <span data-ttu-id="167a1-113">-ServerId</span><span class="sxs-lookup"><span data-stu-id="167a1-113">-ServerId</span></span>
<span data-ttu-id="167a1-114">Anger ID för den auktoriseringsprincip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="167a1-114">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="167a1-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="167a1-115">-Confirm</span></span>
<span data-ttu-id="167a1-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="167a1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="167a1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="167a1-117">-WhatIf</span></span>
<span data-ttu-id="167a1-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="167a1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="167a1-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="167a1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="167a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167a1-120">-DefaultProfile</span></span>
<span data-ttu-id="167a1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="167a1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="167a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167a1-122">CommonParameters</span></span>
<span data-ttu-id="167a1-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="167a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167a1-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="167a1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167a1-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="167a1-125">INPUTS</span></span>

## <span data-ttu-id="167a1-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="167a1-126">OUTPUTS</span></span>

### <span data-ttu-id="167a1-127">Returtyp</span><span class="sxs-lookup"><span data-stu-id="167a1-127">Boolean</span></span>

## <span data-ttu-id="167a1-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="167a1-128">NOTES</span></span>

## <span data-ttu-id="167a1-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="167a1-129">RELATED LINKS</span></span>

[<span data-ttu-id="167a1-130">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="167a1-130">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="167a1-131">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="167a1-131">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="167a1-132">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="167a1-132">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


