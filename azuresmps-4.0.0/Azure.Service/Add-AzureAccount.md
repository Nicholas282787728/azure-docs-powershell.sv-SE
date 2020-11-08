---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099626"
---
# Add-AzureAccount

## Sammanfattning
Lägger till Azure-kontot till Windows PowerShell.

## FRÅGESYNTAXEN

### Användare (standard)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med cmdleten **Add-AzureAccount** blir ditt Azure-konto och dess abonnemang tillgängliga i Windows PowerShell.
Det är som att logga in på ditt Azure-konto i Windows PowerShell.
Använd cmdleten **Remove-AzureAccount** för att logga ut från kontot.

**AzureAccount** laddar ned information om ditt Azure-konto och sparar det i en prenumerations data fil i din centrala användar profil.
Den får också en åtkomsttoken som gör att Windows PowerShell får åtkomst till ditt Azure-konto åt dig.
När kommandot är klart kan du hantera ditt Azure-konto i Windows PowerShell.

Det finns två sätt att göra ditt Azure-konto tillgängligt för Windows PowerShell.
Du kan använda cmdleten **Add-AzureAccount** , som använder ett Management-token i Azure Active Directory (Azure AD)-autentiseringstoken eller **import-AzurePublishSettingsFile**.
Råd om vilken metod som ska användas finns i [så här ansluter du till prenumerationen](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

När du kör **Add-AzureAccount** visas ett interaktivt fönster där du uppmanas att logga in på ditt Azure-konto.
Denna inloggning är giltig tills åtkomst-token upphör.
När den upphör kan du använda cmdletar som kräver åtkomst till ditt konto för att köra **Add-AzureAccount** igen.

I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

## BESKRIVS

### Exempel 1: Lägg till ett konto
```
PS C:\> Add-AzureAccount
```

Det här kommandot lägger till ett Azure-konto i Windows PowerShell.
När du kör kommandot öppnas ett fönster där du kan begära användar namn och lösen ord för kontot.

### Exempel 2: använda en alternativ fil för abonnemang
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

Det här kommandot använder parametern **SubscriptionDataFile** till att **lägga till AzureAccount** för att lagra konto data i C:\Testing\SDF.xml filen i stället för standard filen.

## MALLPARAMETRAR

### -Autentiseringsuppgift
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Miljö
Anger en Azure-miljö.

En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.
Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.
Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Klient organisationen
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Det går inte att pipe in i denna cmdlet

## VÄRDEN

### Ingen
Denna cmdlet returnerar inte några utdata.

## ANMÄRKNINGAR
* **Add-AzureAccount** (och Azure AD-autentiseringsmetoden) har högre prioritet än **import-AzurePublishSettings** (och hanterings certifikat). Om du använder **Add-AzureAccount** även en gång på ditt konto används AUTENTISERINGSMETODEN Azure AD och hanterings certifikatet ignoreras. Använd cmdleten **Remove-AzureAccount** om du vill ta bort Azure AD-token och återställa hanterings certifikat metoden. Om du vill ha mer information skriver du: **Get-Help Remove-AzureAccount**.
* Felet "dina uppgifter har upphört att gälla. Använd Add-AzureAccount för att logga in igen. " anger att din åtkomsttoken har upphört att gälla och Windows PowerShell inte kan komma åt ditt Azure-konto. Återställ åtkomst till kontot genom att köra **Add-AzureAccount** igen.
* Azure PowerShell-konto och prenumerations-cmdlets hämtar data från data filen för abonnemang, inte från det aktiva Azure-kontot. Om du ändrar ditt konto eller dina prenumerationer utanför Windows PowerShell, till exempel med Azure Management Portal, kör du **Add-AzureAccount** igen för att uppdatera prenumerations data filen.

## RELATERADE LÄNKAR

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


