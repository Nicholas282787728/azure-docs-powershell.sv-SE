---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 90da707ce34c191a33a68473f41555a33c0e35b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745782"
---
# <span data-ttu-id="c5d79-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c5d79-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="c5d79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5d79-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d79-103">Skapar en ny cachemapp</span><span class="sxs-lookup"><span data-stu-id="c5d79-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="c5d79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5d79-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5d79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5d79-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d79-106">Cmdlet **New-AzApiManagementCache** skapar en ny cachemapp i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="c5d79-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="c5d79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5d79-107">EXAMPLES</span></span>

### <span data-ttu-id="c5d79-108">Exempel 1: skapa en ny cachemapp</span><span class="sxs-lookup"><span data-stu-id="c5d79-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="c5d79-109">Cmdletar skapar en ny cachemapp i huvud platsen för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c5d79-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="c5d79-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5d79-110">PARAMETERS</span></span>

### <span data-ttu-id="c5d79-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="c5d79-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="c5d79-112">Arm-ResourceId för Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="c5d79-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="c5d79-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c5d79-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d79-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="c5d79-114">-CacheId</span></span>
<span data-ttu-id="c5d79-115">ID för ny cache.</span><span class="sxs-lookup"><span data-stu-id="c5d79-115">Identifier of new cache.</span></span>
<span data-ttu-id="c5d79-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c5d79-116">This parameter is optional.</span></span>
<span data-ttu-id="c5d79-117">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="c5d79-117">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d79-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c5d79-118">-ConnectionString</span></span>
<span data-ttu-id="c5d79-119">Redis anslutnings sträng.</span><span class="sxs-lookup"><span data-stu-id="c5d79-119">Redis Connection String.</span></span>
<span data-ttu-id="c5d79-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c5d79-120">This parameter is required.</span></span>

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

### <span data-ttu-id="c5d79-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c5d79-121">-Context</span></span>
<span data-ttu-id="c5d79-122">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c5d79-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c5d79-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c5d79-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d79-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d79-124">-DefaultProfile</span></span>
<span data-ttu-id="c5d79-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d79-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d79-126">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c5d79-126">-Description</span></span>
<span data-ttu-id="c5d79-127">Cachestorlek.</span><span class="sxs-lookup"><span data-stu-id="c5d79-127">Cache Description.</span></span>
<span data-ttu-id="c5d79-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c5d79-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d79-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5d79-129">-Confirm</span></span>
<span data-ttu-id="c5d79-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5d79-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5d79-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5d79-131">-WhatIf</span></span>
<span data-ttu-id="c5d79-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c5d79-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5d79-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c5d79-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5d79-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d79-134">CommonParameters</span></span>
<span data-ttu-id="c5d79-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5d79-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d79-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5d79-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d79-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5d79-137">INPUTS</span></span>

### <span data-ttu-id="c5d79-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c5d79-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c5d79-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c5d79-139">System.String</span></span>

## <span data-ttu-id="c5d79-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5d79-140">OUTPUTS</span></span>

### <span data-ttu-id="c5d79-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c5d79-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="c5d79-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5d79-142">NOTES</span></span>

## <span data-ttu-id="c5d79-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5d79-143">RELATED LINKS</span></span>

[<span data-ttu-id="c5d79-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c5d79-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="c5d79-145">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c5d79-145">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="c5d79-146">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="c5d79-146">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)