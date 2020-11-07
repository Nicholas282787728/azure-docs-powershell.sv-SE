---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920094"
---
# <span data-ttu-id="66799-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="66799-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="66799-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66799-102">SYNOPSIS</span></span>
<span data-ttu-id="66799-103">Får ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="66799-103">Gets a resource lock.</span></span>

## <span data-ttu-id="66799-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66799-104">SYNTAX</span></span>

### <span data-ttu-id="66799-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66799-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66799-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="66799-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66799-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="66799-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66799-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="66799-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66799-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="66799-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66799-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="66799-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66799-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="66799-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66799-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66799-112">DESCRIPTION</span></span>
<span data-ttu-id="66799-113">Cmdleten **Get-AzResourceLock** får Azure Resource lock.</span><span class="sxs-lookup"><span data-stu-id="66799-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="66799-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66799-114">EXAMPLES</span></span>

### <span data-ttu-id="66799-115">Exempel 1: skaffa ett lås</span><span class="sxs-lookup"><span data-stu-id="66799-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="66799-116">Det här kommandot får resurs låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="66799-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="66799-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66799-117">PARAMETERS</span></span>

### <span data-ttu-id="66799-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66799-118">-ApiVersion</span></span>
<span data-ttu-id="66799-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="66799-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="66799-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="66799-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="66799-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="66799-121">-AtScope</span></span>
<span data-ttu-id="66799-122">Anger att denna cmdlet returnerar alla lås på eller ovanför det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="66799-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="66799-123">Om du inte anger den här parametern returnerar cmdleten alla lås på, ovanför eller under scopet.</span><span class="sxs-lookup"><span data-stu-id="66799-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="66799-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66799-124">-DefaultProfile</span></span>
<span data-ttu-id="66799-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="66799-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66799-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="66799-126">-LockId</span></span>
<span data-ttu-id="66799-127">Anger ID för det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="66799-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="66799-128">-LockName</span><span class="sxs-lookup"><span data-stu-id="66799-128">-LockName</span></span>
<span data-ttu-id="66799-129">Anger namnet på det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="66799-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="66799-130">-För</span><span class="sxs-lookup"><span data-stu-id="66799-130">-Pre</span></span>
<span data-ttu-id="66799-131">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="66799-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66799-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66799-132">-ResourceGroupName</span></span>
<span data-ttu-id="66799-133">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="66799-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="66799-134">Denna cmdlet hämtar lås för den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="66799-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="66799-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="66799-135">-ResourceName</span></span>
<span data-ttu-id="66799-136">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="66799-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="66799-137">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="66799-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="66799-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="66799-138">-ResourceType</span></span>
<span data-ttu-id="66799-139">Anger resurs typen för den resurs som den här låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="66799-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="66799-140">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="66799-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="66799-141">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="66799-141">-Scope</span></span>
<span data-ttu-id="66799-142">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="66799-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="66799-143">Cmdleten får lås för detta scope.</span><span class="sxs-lookup"><span data-stu-id="66799-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="66799-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="66799-144">-TenantLevel</span></span>
<span data-ttu-id="66799-145">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="66799-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="66799-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66799-146">CommonParameters</span></span>
<span data-ttu-id="66799-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66799-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66799-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66799-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66799-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66799-149">INPUTS</span></span>

### <span data-ttu-id="66799-150">System. String</span><span class="sxs-lookup"><span data-stu-id="66799-150">System.String</span></span>

## <span data-ttu-id="66799-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66799-151">OUTPUTS</span></span>

### <span data-ttu-id="66799-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="66799-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="66799-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66799-153">NOTES</span></span>

## <span data-ttu-id="66799-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66799-154">RELATED LINKS</span></span>

[<span data-ttu-id="66799-155">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="66799-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="66799-156">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="66799-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="66799-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="66799-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


