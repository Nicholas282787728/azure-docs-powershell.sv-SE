---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: a8c1aa2d0f22a9c6dc6260384e51140cb930106a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583048"
---
# <span data-ttu-id="bf03a-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bf03a-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="bf03a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf03a-102">SYNOPSIS</span></span>
<span data-ttu-id="bf03a-103">Uppdaterar ett befintligt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="bf03a-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf03a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf03a-104">SYNTAX</span></span>

### <span data-ttu-id="bf03a-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf03a-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf03a-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf03a-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf03a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf03a-107">DESCRIPTION</span></span>
<span data-ttu-id="bf03a-108">Uppdaterar ett befintligt Azure Active Directory-program.</span><span class="sxs-lookup"><span data-stu-id="bf03a-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="bf03a-109">Använd New-AzureRmADAppCredential cmdlet för att uppdatera autentiseringsuppgifterna för det här programmet.</span><span class="sxs-lookup"><span data-stu-id="bf03a-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="bf03a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf03a-110">EXAMPLES</span></span>

### <span data-ttu-id="bf03a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bf03a-111">Example 1</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="bf03a-112">Uppdaterar egenskaperna för ett befintligt Azure Active Directory-program med objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="bf03a-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="bf03a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bf03a-113">Example 2</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="bf03a-114">Uppdaterar visnings namnet för ett befintligt Azure Active Directory-program med objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="bf03a-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="bf03a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf03a-115">PARAMETERS</span></span>

### <span data-ttu-id="bf03a-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bf03a-116">-ApplicationId</span></span>
<span data-ttu-id="bf03a-117">ID för programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="bf03a-117">The id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03a-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="bf03a-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="bf03a-119">Det värde som anger om programmet uppdateras till en enskild klient organisation eller en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="bf03a-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf03a-120">-DefaultProfile</span></span>
<span data-ttu-id="bf03a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf03a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf03a-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bf03a-122">-DisplayName</span></span>
<span data-ttu-id="bf03a-123">Nytt visnings namn för programmet.</span><span class="sxs-lookup"><span data-stu-id="bf03a-123">New Display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03a-124">-Start Sidan</span><span class="sxs-lookup"><span data-stu-id="bf03a-124">-HomePage</span></span>
<span data-ttu-id="bf03a-125">Ny URL för programmets start sida.</span><span class="sxs-lookup"><span data-stu-id="bf03a-125">New URL of the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03a-126">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="bf03a-126">-IdentifierUris</span></span>
<span data-ttu-id="bf03a-127">Nya URI: er som identifierar programmet.</span><span class="sxs-lookup"><span data-stu-id="bf03a-127">New URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03a-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bf03a-128">-ObjectId</span></span>
<span data-ttu-id="bf03a-129">Objekt-ID för programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="bf03a-129">The object id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03a-130">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="bf03a-130">-ReplyUrls</span></span>
<span data-ttu-id="bf03a-131">Nya svars-URL: er för programmet.</span><span class="sxs-lookup"><span data-stu-id="bf03a-131">New reply urls for the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf03a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf03a-132">-Confirm</span></span>
<span data-ttu-id="bf03a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf03a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf03a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf03a-134">-WhatIf</span></span>
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

### <span data-ttu-id="bf03a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf03a-135">CommonParameters</span></span>
<span data-ttu-id="bf03a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf03a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf03a-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf03a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf03a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf03a-138">INPUTS</span></span>

### <span data-ttu-id="bf03a-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="bf03a-139">None</span></span>
<span data-ttu-id="bf03a-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bf03a-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf03a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf03a-141">OUTPUTS</span></span>

### <span data-ttu-id="bf03a-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="bf03a-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="bf03a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf03a-143">NOTES</span></span>

## <span data-ttu-id="bf03a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf03a-144">RELATED LINKS</span></span>

[<span data-ttu-id="bf03a-145">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bf03a-145">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="bf03a-146">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bf03a-146">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="bf03a-147">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bf03a-147">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="bf03a-148">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bf03a-148">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="bf03a-149">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bf03a-149">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="bf03a-150">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bf03a-150">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

