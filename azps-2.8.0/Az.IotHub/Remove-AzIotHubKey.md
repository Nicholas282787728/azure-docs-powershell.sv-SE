---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: eb0ec4390cb8e354707109ecafb5d284b70fa910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743971"
---
# <span data-ttu-id="d78cf-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="d78cf-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="d78cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d78cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d78cf-103">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="d78cf-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="d78cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d78cf-104">SYNTAX</span></span>

### <span data-ttu-id="d78cf-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d78cf-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d78cf-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d78cf-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d78cf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d78cf-107">DESCRIPTION</span></span>
<span data-ttu-id="d78cf-108">Tar bort en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="d78cf-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="d78cf-109">Om det finns flera tangenter med samma namn tas den första i listan bort.</span><span class="sxs-lookup"><span data-stu-id="d78cf-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="d78cf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d78cf-110">EXAMPLES</span></span>

### <span data-ttu-id="d78cf-111">Exempel 1 ta bort en IotHub</span><span class="sxs-lookup"><span data-stu-id="d78cf-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="d78cf-112">Tar bort den iothubowner1 från IotHub som heter "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d78cf-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d78cf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d78cf-113">PARAMETERS</span></span>

### <span data-ttu-id="d78cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78cf-114">-DefaultProfile</span></span>
<span data-ttu-id="d78cf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d78cf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d78cf-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="d78cf-116">-HubId</span></span>
<span data-ttu-id="d78cf-117">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="d78cf-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d78cf-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d78cf-118">-KeyName</span></span>
<span data-ttu-id="d78cf-119">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="d78cf-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d78cf-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d78cf-120">-Name</span></span>
<span data-ttu-id="d78cf-121">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="d78cf-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d78cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="d78cf-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d78cf-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d78cf-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d78cf-124">-Confirm</span></span>
<span data-ttu-id="d78cf-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d78cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d78cf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d78cf-126">-WhatIf</span></span>
<span data-ttu-id="d78cf-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d78cf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d78cf-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d78cf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d78cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78cf-129">CommonParameters</span></span>
<span data-ttu-id="d78cf-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d78cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78cf-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d78cf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78cf-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d78cf-132">INPUTS</span></span>

### <span data-ttu-id="d78cf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d78cf-133">System.String</span></span>

## <span data-ttu-id="d78cf-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d78cf-134">OUTPUTS</span></span>

### <span data-ttu-id="d78cf-135">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d78cf-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="d78cf-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d78cf-136">NOTES</span></span>

## <span data-ttu-id="d78cf-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d78cf-137">RELATED LINKS</span></span>
