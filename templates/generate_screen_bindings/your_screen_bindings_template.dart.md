````dart
//.title
// ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓
//
// GENERATED BY XYZ_GEN - DO NOT MODIFY BY HAND
// See: https://github.com/robmllze/xyz_gen
//
// ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓
//.title~

part of "___CLASS_FILE___";

// ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░

const _IS_ACCESSIBLE_ONLY_IF_LOGGED_IN_AND_VERIFIED = ___IS_ACCESSIBLE_ONLY_IF_LOGGED_IN_AND_VERIFIED___;
const _IS_ACCESSIBLE_ONLY_IF_LOGGED_IN = ___IS_ACCESSIBLE_ONLY_IF_LOGGED_IN___;
const _IS_ACCESSIBLE_ONLY_IF_LOGGED_OUT = ___IS_ACCESSIBLE_ONLY_IF_LOGGED_OUT___;
const _IS_REDIRECTABLE = ___IS_REDIRECTABLE___;

const _CLASS = "___CLASS___";
const _SEGMENT = "___SCREEN_SEGMENT___";
const _PATH = "/$_SEGMENT";
const _TR_KEY = "screens.___CLASS___";

// ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░

extension _ScreenTr on String {
  String screenTr([Map<dynamic, dynamic> args = const {}]) {
    return this.splitByLastOccurrenceOf("||").join("||$_TR_KEY.").tr(args);
  }
}

// ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░

Screen? maker___CLASS___(
  ModelScreenConfiguration configuration,
  bool isLoggedInAndVerified,
  bool isLoggedIn,
  bool isLoggedOut,
) {
  if ((_IS_ACCESSIBLE_ONLY_IF_LOGGED_IN_AND_VERIFIED && !isLoggedInAndVerified) || (_IS_ACCESSIBLE_ONLY_IF_LOGGED_IN && !isLoggedIn) || (_IS_ACCESSIBLE_ONLY_IF_LOGGED_OUT && !isLoggedOut)) {
    return null;
  }
  if (configuration is ___CONFIGURATION_CLASS___ ||
      RegExp(
        r"^(" + _PATH + r")([?/].*)?$",
      ).hasMatch(
        Uri.decodeComponent(
          configuration.path ?? "",
        ),
      )) {
    return ___CLASS___(
      key: ValueKey<String?>(configuration.path),
      configuration: configuration,
    );
  }
  return null;
}

// ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░

class ___CONFIGURATION_CLASS___ extends ModelScreenConfiguration {
  static const CLASS = _CLASS;
  static const SEGMENT = _SEGMENT;
  static const PATH = _PATH;
  static const TR_KEY = _TR_KEY;
  static const IS_ACCESSIBLE_ONLY_IF_LOGGED_IN = _IS_ACCESSIBLE_ONLY_IF_LOGGED_IN;
    static const IS_ACCESSIBLE_ONLY_IF_LOGGED_IN_AND_VERIFIED = _IS_ACCESSIBLE_ONLY_IF_LOGGED_IN_AND_VERIFIED;
  static const IS_ACCESSIBLE_ONLY_IF_LOGGED_OUT = _IS_ACCESSIBLE_ONLY_IF_LOGGED_OUT;
  static const IS_REDIRECTABLE = _IS_REDIRECTABLE;
  static const NAVIGATION_CONTROLS_WIDGET = ___NAVIGATION_CONTROLS_WIDGET___;
  static const TITLE = "___DEFAULT_TITLE___||title";
  // ignore: prefer_const_declarations
  static final ScreenMakeup? screenMakeup = ___MAKEUP___;
  
  ___IP0___
  ___QP0___
  ___PS0___

  ___CONFIGURATION_CLASS___({
    ___IP1___
    ___QP1___
    ___PS1___
    Map<dynamic, dynamic>? $arguments,
  }): super(
    path: _PATH,
    arguments: {
      ___IP2___
      ___QP2___
      ___PS2___
      ...?$arguments,
    },
    isAccessibleOnlyIfLoggedInAndVerified: _IS_ACCESSIBLE_ONLY_IF_LOGGED_IN_AND_VERIFIED,
    isAccessibleOnlyIfLoggedIn: _IS_ACCESSIBLE_ONLY_IF_LOGGED_IN,
    isAccessibleOnlyIfLoggedOut: _IS_ACCESSIBLE_ONLY_IF_LOGGED_OUT,
    isRedirectable: _IS_REDIRECTABLE,
  ) {
    super.navigationControlsWidget = NAVIGATION_CONTROLS_WIDGET;
    super.title = TITLE.screenTr();
    super.makeup = screenMakeup;
  }

  ___CONFIGURATION_CLASS___.fromArgs(Map<dynamic, dynamic>? args)
      : super(
          path: _PATH,
          arguments: args,
          isAccessibleOnlyIfLoggedInAndVerified: _IS_ACCESSIBLE_ONLY_IF_LOGGED_IN_AND_VERIFIED,
          isAccessibleOnlyIfLoggedIn: _IS_ACCESSIBLE_ONLY_IF_LOGGED_IN,
          isAccessibleOnlyIfLoggedOut: _IS_ACCESSIBLE_ONLY_IF_LOGGED_OUT,
          isRedirectable: _IS_REDIRECTABLE,
        ) {
    super.navigationControlsWidget = NAVIGATION_CONTROLS_WIDGET;
    super.title = TITLE.screenTr();
    super.makeup = screenMakeup;
  }
}

// ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░

abstract class _ControllerBroker<T1 extends ___CLASS___, T2 extends _View>
    extends ScreenController<___CONFIGURATION_CLASS___> {

  late final screen = super.superScreen as T1;
  late final state = super.superState as T2;
  late final configuration = ___CONFIGURATION_CLASS___.fromArgs(
    screen.configuration?.arguments ?? {},
  );
  
  _ControllerBroker(super.superScreen, super.superState);
}

// ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░

final generated___CLASS___Route = GoRoute(
  path: _SEGMENT,
  pageBuilder: (_, GoRouterState state) {
    final extraConfiguration = letAs<ModelScreenConfiguration>(state.extra);
    final urlConfiguration = urlToScreenConfiguration(
      url: state.uri,
      isAccessibleOnlyIfLoggedIn: ___CONFIGURATION_CLASS___.IS_ACCESSIBLE_ONLY_IF_LOGGED_IN,
      isAccessibleOnlyIfLoggedInAndVerified: ___CONFIGURATION_CLASS___.IS_ACCESSIBLE_ONLY_IF_LOGGED_IN_AND_VERIFIED,
      isAccessibleOnlyIfLoggedOut: ___CONFIGURATION_CLASS___.IS_ACCESSIBLE_ONLY_IF_LOGGED_OUT,
      isRedirectable: ___CONFIGURATION_CLASS___.IS_REDIRECTABLE,
      makeup: ___CONFIGURATION_CLASS___.screenMakeup,
      navigationControlsWidget: ___CONFIGURATION_CLASS___.NAVIGATION_CONTROLS_WIDGET,
      title: ___CONFIGURATION_CLASS___.TITLE.screenTr(),
    );
    final configuration = extraConfiguration ?? urlConfiguration;
    return NoTransitionPage(
      key: state.pageKey,
      child: ___CLASS___(
        key: ValueKey<String?>(configuration.path),
        configuration: configuration,
      ),
    );
  },
);

// ░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░

typedef T___CLASS___Controller =  _ControllerBroker<___CLASS___, _View>;

typedef T___CLASS___View = ScreenView<___CLASS___, ___CONFIGURATION_CLASS___, ___CLASS___Controller>;

typedef T___CLASS___PageView<T extends ScreenPage> = ScreenPageView<T, ___CONFIGURATION_CLASS___, ___CLASS___Controller>;
````