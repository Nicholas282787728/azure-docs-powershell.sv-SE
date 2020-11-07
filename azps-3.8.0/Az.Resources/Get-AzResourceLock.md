---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926757"
---
# <span data-ttu-id="badb3-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="badb3-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="badb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="badb3-102">SYNOPSIS</span></span>
<span data-ttu-id="badb3-103">Får ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="badb3-103">Gets a resource lock.</span></span>

## <span data-ttu-id="badb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="badb3-104">SYNTAX</span></span>

### <span data-ttu-id="badb3-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="badb3-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="badb3-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="badb3-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="badb3-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="badb3-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="badb3-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="badb3-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="badb3-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="badb3-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="badb3-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="badb3-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="badb3-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="badb3-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="badb3-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="badb3-112">DESCRIPTION</span></span>
<span data-ttu-id="badb3-113">Cmdleten **Get-AzResourceLock** får Azure Resource lock.</span><span class="sxs-lookup"><span data-stu-id="badb3-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="badb3-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="badb3-114">EXAMPLES</span></span>

### <span data-ttu-id="badb3-115">Exempel 1: skaffa ett lås</span><span class="sxs-lookup"><span data-stu-id="badb3-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="badb3-116">Det här kommandot får resurs låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="badb3-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="badb3-117">Exempel 2: Hämta lås på resurs grupps nivå eller högre</span><span class="sxs-lookup"><span data-stu-id="badb3-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="badb3-118">Det här kommandot får resursens lås för resurs gruppen eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="badb3-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="badb3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="badb3-119">PARAMETERS</span></span>

### <span data-ttu-id="badb3-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="badb3-120">-ApiVersion</span></span>
<span data-ttu-id="badb3-121">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="badb3-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="badb3-122">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="badb3-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badb3-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="badb3-123">-AtScope</span></span>
<span data-ttu-id="badb3-124">Anger att denna cmdlet returnerar alla lås på eller ovanför det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="badb3-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="badb3-125">Om du inte anger den här parametern returnerar cmdleten alla lås på, ovanför eller under scopet.</span><span class="sxs-lookup"><span data-stu-id="badb3-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="badb3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="badb3-126">-DefaultProfile</span></span>
<span data-ttu-id="badb3-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="badb3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="badb3-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="badb3-128">-LockId</span></span>
<span data-ttu-id="badb3-129">Anger ID för det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="badb3-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="badb3-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="badb3-130">-LockName</span></span>
<span data-ttu-id="badb3-131">Anger namnet på det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="badb3-131">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="badb3-132">-För</span><span class="sxs-lookup"><span data-stu-id="badb3-132">-Pre</span></span>
<span data-ttu-id="badb3-133">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="badb3-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="badb3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="badb3-134">-ResourceGroupName</span></span>
<span data-ttu-id="badb3-135">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="badb3-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="badb3-136">Denna cmdlet hämtar lås för den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="badb3-136">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="badb3-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="badb3-137">-ResourceName</span></span>
<span data-ttu-id="badb3-138">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="badb3-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="badb3-139">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="badb3-139">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="badb3-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="badb3-140">-ResourceType</span></span>
<span data-ttu-id="badb3-141">Anger resurs typen för den resurs som den här låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="badb3-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="badb3-142">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="badb3-142">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="badb3-143">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="badb3-143">-Scope</span></span>
<span data-ttu-id="badb3-144">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="badb3-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="badb3-145">Cmdleten får lås för detta scope.</span><span class="sxs-lookup"><span data-stu-id="badb3-145">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="badb3-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="badb3-146">-TenantLevel</span></span>
<span data-ttu-id="badb3-147">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="badb3-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badb3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="badb3-148">CommonParameters</span></span>
<span data-ttu-id="badb3-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="badb3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="badb3-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="badb3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="badb3-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="badb3-151">INPUTS</span></span>

### <span data-ttu-id="badb3-152">System. String</span><span class="sxs-lookup"><span data-stu-id="badb3-152">System.String</span></span>

## <span data-ttu-id="badb3-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="badb3-153">OUTPUTS</span></span>

### <span data-ttu-id="badb3-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="badb3-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="badb3-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="badb3-155">NOTES</span></span>

## <span data-ttu-id="badb3-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="badb3-156">RELATED LINKS</span></span>

[<span data-ttu-id="badb3-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="badb3-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="badb3-158">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="badb3-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="badb3-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="badb3-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


